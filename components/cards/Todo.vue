<template>
  	<div class="todo">
		<div class="" v-if="data.mode">
			<div class="text subtitle base-color">{{data.title}}</div>
			<div class="todo-content">
				<ul class="todo-list d-flex flex-column justify-content-start align-items-start">
					<li v-for="(l, index) in data.list" class="todo-list-item">
						<table>
							<tr>
								<td style="width: 20px"><input type="checkbox" v-model="data.list[index].status" :id="l.id" class="pull-left"/></td>
								<td>
									<label :for="l.id"  class="text black">{{l.value}}</label>
								</td>
								<td>
									<label class="remove" @click="remove(index)"></label>
								</td>
							</tr>
						</table>
					</li>
					
				</ul>
				<div class="todo-fields">
					<li>
						<input class="todo-input" v-model="newVal" placeholder="Type your task" @keyup.enter="addTodo"/>
					</li>
					<div class="todo-buttons d-flex justify-content-between align-items-start">
						<button @click="switchMode" class="field-button edit-button">
						<span>Edit</span> 
						</button>
						<button class="field-button doing-button" @click="changeStatusDoing($event)">
						<span>Doing</span> 
						</button>
						<button class="field-button done-button" @click="changeStatusDone($event)">
						<span>Done</span> 
						</button>
						<button class="field-button close-button" @click="deleteFunc(index)">
							<span>X</span> 
						</button>
					</div>
				</div>	
			</div>
		</div>

		<div class="todo-edit" v-else>
			<div class="">
				<input type="text" v-model="data.title"/>
			</div>
			<div class="panel-body">
				<ul class="todo-list">
					<li v-for="(l, index) in data.list">
						<input type="text" class="todo-input"  v-model="data.list[index].value"/>
					</li>
				</ul>
				<button @click="switchMode" class="field-button save-button">
					<span>Save</span>
				</button>
			</div>
		</div>
	</div>

</template>

<script>
	export default {
		name: 'todo',
		props:[
			"data", 
			"index", 
			"deleteFunc"
		],
		data() {
			return {
				newVal: ''
			}
		},
		methods: {
			addTodo(){
				if(this.newVal !== "") this.data.list.push({value: this.newVal, status: false, id: Date.now()});
				this.newVal = '';
				
			},
			switchMode(){
				this.data.mode = !this.data.mode;
			},
			remove(index){
				this.data.list.splice(index, 1);
			},
			changeStatusDoing(index) {
				console.log('index', index)
				this.data.option = 'doing'
				let elem = index.target.closest(".todo")
				elem.classList.remove('done')
				elem.classList.add('doing')
			},
			changeStatusDone(index) {
				this.data.option = 'done'
				let elem = index.target.closest(".todo")
				elem.classList.remove('doing')
				elem.classList.add('done')
			}
		}
	}
</script>