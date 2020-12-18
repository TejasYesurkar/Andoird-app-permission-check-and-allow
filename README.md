# Andoird-app-permission-check-and-allow

                  String requiredPermission = Manifest.permission.CAMERA;
                  int checkVal = mContext.checkCallingOrSelfPermission(requiredPermission);
                  if (checkVal== PackageManager.PERMISSION_GRANTED){

                      Toast.makeText(mContext, "Permssion Granted Successfully", Toast.LENGTH_SHORT).show();
                   
                  }else{
                      holder.chkitem.setChecked(false);
                      ActivityCompat.requestPermissions((Activity) mContext, new String[] {Manifest.permission.CAMERA}, 2);
                      Toast.makeText(mContext, "Please allow camera permission first", Toast.LENGTH_SHORT).show();
                  }
