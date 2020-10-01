<template>
  <div id="my-strictly-unique-vue-upload-multiple-image" style="display: flex; justify-content: center;">
    <VueUploadMultipleImage
      @upload-success="uploadImageSuccess"
      @before-remove="beforeRemove"
      @edit-image="editImage"
      :data-images="images"
      idUpload="myIdUpload"
      editUpload="myIdEdit"
      dragText = "Drag an image here"
      browseText = "(or click here to browse)"
      primaryText = "Default Image"
      markIsPrimaryText = "Set as default image"
      popupText = "This image will be set as default"
      dropText = "Drag and drop"
      accept = image/jpeg,image/png,image/jpg,image/tif,image/tiff
    ></VueUploadMultipleImage>
  </div>
</template>

<script>

export default {
  name: "AppUpload",
  data(){
    return{
      file:"",
      images: []
    }
  },
  methods:{

    uploadImageSuccess(formData, index, fileList) {    },
    beforeRemove (index, done, fileList) {    },
    editImage (formData, index, fileList) {   },
  }
}
</script>

<style scoped>

</style>
