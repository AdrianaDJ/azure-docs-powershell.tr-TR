---
title: Az 2.0.0 için geçiş kılavuzu
description: Bu geçiş kılavuzu, Azure PowerShell Az sürüm 2.0'da yapılan yeni değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 5f15d1a4f1e8416d7214aceb78494867fe4aad52
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052881"
---
# <a name="migration-guide-for-az-200"></a>Az 2.0.0 için Geçiş Kılavuzu

Bu belgede Az modülünün 1.0.0 ile 2.0.0 sürümleri arasındaki değişiklikler açıklanır 

## <a name="table-of-contents"></a>İçindekiler
- [Modüldeki yeni değişiklikler](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>Modüldeki yeni değişiklikler

### <a name="azcompute"></a>Az.Compute

- `New-AzAvailabilitySet` ve `Update-AzAvailabilitySet` cmdlet'lerinden `Managed` parametresi kaldırıldı, artık ```Sku = Aligned``` kullanılıyor

  #### <a name="before"></a>Önce

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- Tutarlılık sağlamak için `Update-AzImage` cmdlet'inde 'ByName' ve 'ByResourceId' parametre kümelerinden `Image` parametresi kaldırıldı 
  
  #### <a name="before"></a>Önce

  Aşağıdaki kodun işlevsel olduğuna ama geçirilen ImageName değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- Tutarlılık sağlamak için `Restart-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı
  
  #### <a name="before"></a>Önce

  Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- Tutarlılık sağlamak için `Start-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı
  
  #### <a name="before"></a>Önce

  Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- Tutarlılık sağlamak için `Stop-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı
  
  #### <a name="before"></a>Önce

  Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- Tutarlılık sağlamak için `Remove-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı
  
  #### <a name="before"></a>Önce

  Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- Tutarlılık sağlamak için `Set-AzVM` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı
  
  #### <a name="before"></a>Önce

  Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- Tutarlılık sağlamak için `Save-AzVMImage` cmdlet'inde 'ByObject' ve 'ByResourceId' parametre kümelerinden `Name` parametresi kaldırıldı 
  
  #### <a name="before"></a>Önce
  Aşağıdaki kodun işlevsel olduğuna ama geçirilen Name değerinin kullanılmadığına dikkat edin. Dolayısıyla bu parametrenin kaldırılması işlevi etkilemez.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>Sonra
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- `PSVirtualMachineScaleSetVM` içinde `ProtectFromScaleIn` özelliğini kapsüllemek için ProtectionPolicy özelliği eklendi

  #### <a name="before"></a>Önce

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- `EncryptionSettings` özelliğini `PSDisk` içine almak için ```EncryptionSettingsCollection``` Özelliği eklendi

  #### <a name="before"></a>Önce

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- `EncryptionSettings` özelliğini `PSSnapshot` içine almak için ```EncryptionSettingsCollection``` Özelliği eklendi

  #### <a name="before"></a>Önce

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- `PSVirtualMachineScaleSet` içinden `VirtualMachineProfile` özelliği kaldırıldı

  #### <a name="before"></a>Önce

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- `Set-AzVMBootDiagnostic` cmdlet'inin `Set-AzVMBootDiagnostics` diğer adı kaldırıldı

  #### <a name="before"></a>Önce

  Kullanım dışı bırakılan diğer ad kullanılıyor

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- `Export-AzLogAnalyticThrottledRequest` cmdlet'inin `Export-AzLogAnalyticThrottledRequests` diğer adı kaldırıldı

  #### <a name="before"></a>Önce

  Kullanım dışı bırakılan diğer ad kullanılıyor

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- `Grant-AzHDInsightHttpServicesAccess` ve `Revoke-AzHDInsightHttpServicesAccess` cmdlet'leri kaldırıldı. Tüm HDInsight kümelerinde HTTP erişimi her zaman etkin olduğundan artık bunlar gerekli değildir.
- Yeni `Set-AzHDInsightGatewayCredential` cmdlet'i eklendi. Ağ geçidi HTTP kullanıcı adını ve parolasını değiştirmek için bu cmdlet'i kullanın (`Grant-AzHDInsightHttpServicesAccess` cmdlet'inin yerini aldı).
- `Get-AzHDInsightJobOutput` cmdlet'i depolama anahtarına ayrıntılı rol tabanlı erişimi destekleyecek şekilde güncelleştirildi.
    - HDInsight Küme Operatörü, Katkıda Bulunan veya Sahip rolleri olan kullanıcılar etkilenmeyecek.
    - Yalnızca Okuyucu rolüne sahip kullanıcıların `DefaultStorageAccountKey` parametresini açık olarak belirtmesi gerekecek.

Bu rol tabanlı erişim değişiklikleri hakkında daha fazla bilgi için bkz. [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)

  #### <a name="before"></a>Önce

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Get-AzHDInsightJobOutput cmdlet'i için yalnızca Okuyucu rolü olan kullanıcılar

  ####  <a name="before"></a>Önce

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>Sonra

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Blob, Kuyruk ve Dosya cmdlet'lerinden döndürülen türlerin `Microsoft.WindowsAzure.Storage` olan ad alanları `Microsoft.Azure.Storage` olarak değiştirildi.  Bu hataya neden olan değişiklik ilkesine göre teknik açıdan hataya neden olan bir değişiklik olmasa da, bu cmdlet'lerden döndürülen nesnelerle etkileşim kurmak için Storage .Net SDK'sındaki yöntemleri kullanan kodlarda bazı değişiklikler yapmak gerekebilir.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>Örnek 1:  Kuyruğa bir ileti ekleyin (CloudQueueMessage nesnesi ad alanını değiştirin)

  Önce: 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  Sonra:

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>Örnek 2:  AccessCondition ile Blob/Dosya Özniteliklerini getirin (AccessCondition nesnesi ad alanını değiştirin)

  Önce: 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  Sonra:

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Teknik açıdan hataya neden olan bir değişiklik olmasa da, `New/Get/Set-AzStorageAccount` cmdlet'lerinden döndürülen Depolama Hesaplarının Sku.Name özelliğinde aşağıdaki gibi bazı çıkış farklılıkları göreceksiniz. (Değişiklik sonrasında, çıkış ve giriş SkuName adları uyumlu olur.)
  - "StandardLRS" -> "Standard_LRS";
  - "StandardGRS" -> "Standard_GRS";
  - "StandardRAGRS" -> "Standard_RAGRS";
  - "StandardZRS" -> "Standard_ZRS";
  - "PremiumLRS" -> "Premium_LRS";

- Kind belirtmeden depolama hesabı oluştururken varsayılan hizmet davranışı değişti.  Önceki sürümlerde `Kind` belirtilmeden bir depolama hesabı oluşturulduğunda Depolama hesabında Kind değeri olarak `Storage` kullanılıyordu; yeni sürümde varsayılan `Kind` değeri `StorageV2` oldu. Kind değeri 'Storage' olan bir V1 Depolama hesabı oluşturmanız gerekiyorsa '-Kind Storage' parametresini ekleyin

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Örnek: Depolama hesabı oluşturun (Varsayılan Kind değişikliği)  

  Önce:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  Sonra:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
