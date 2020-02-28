<template>
    <q-page padding>
        <div class="row q-mb-lg">
            <q-input v-model="text" placeholder="Add New Task" class="col" /><q-btn color="primary" size="sm" label="Add" />
        </div>
        <div class="row">
            <div class="q-pa-md q-gutter-md col">
                <q-list bordered padding class="rounded-borders">
                    <q-item-label header>Tasks</q-item-label>

                    <q-item clickable v-ripple v-bind:key="index" v-for="(task, index) in tasks">
                        <q-item-section avatar top>
                            <q-avatar icon="folder" color="primary" text-color="white" />
                        </q-item-section>

                        <q-item-section>
                            <q-item-label lines="1">{{task}}</q-item-label>
                            <q-item-label caption>February 22nd, 2019</q-item-label>
                        </q-item-section>

                        <q-item-section side>
                            <q-icon name="check" color="green" />
                        </q-item-section>
                    </q-item>
                </q-list>
            </div>
        </div>
    </q-page>
</template>

<script>
export default {
    name: 'PageIndex',
    data() {
        return {
            tasks: [
                'Wake up',
                'Brush Teeth',
                'Shower'
            ]
        }
    }
}
</script>
