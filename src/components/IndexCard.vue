<template>
    <el-card shadow="always" >
        <template #header>
            <div class=" flex justify-between">
                <span class="text-sm">{{ title }}</span>
                <el-tag type="danger" effect="plain">
                    {{ tips }}
                </el-tag>
            </div>
        </template>
        <!-- card body -->

        <el-row :gutter="20">
            <el-col :span="6" :offset="0" v-for="(item, index) in btns" :key="index">
                <el-card shadow="hover" class="border-0 bg-light-300">
                    <div class="flex flex-col justify-center items-center">
                        <span class="text-xl mb-2">{{ item.value }}</span>
                        <span class="text-xs text-gray-500">{{ item.label }}</span>
                    </div>
                </el-card>
            </el-col>
        </el-row>
        
    </el-card>
    
</template>

<script setup>
    defineProps({
        title: String,
        tips: String,
        btns: Array,
    })
</script>