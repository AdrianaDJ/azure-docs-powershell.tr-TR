---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280206"
---
# <span data-ttu-id="fa9c9-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="fa9c9-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="fa9c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9c9-103">Yönetilen bir HSM yedeklemeden tümüyle geri yükler.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="fa9c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa9c9-104">SYNTAX</span></span>

### <span data-ttu-id="fa9c9-105">InteractiveStorageName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa9c9-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9c9-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="fa9c9-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9c9-107">Inputobjectstorageuri</span><span class="sxs-lookup"><span data-stu-id="fa9c9-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9c9-108">Inputobjectstoragename</span><span class="sxs-lookup"><span data-stu-id="fa9c9-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9c9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa9c9-109">DESCRIPTION</span></span>
<span data-ttu-id="fa9c9-110">Yönetilen bir HSM 'yi depolama hesabında depolanan bir yedekten tümüyle geri yükler.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="fa9c9-111">`Backup-AzManagedHsm`Yedekleme için kullanın.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="fa9c9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa9c9-112">EXAMPLES</span></span>

### <span data-ttu-id="fa9c9-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa9c9-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="fa9c9-114">Örnek, "https://{accountName}. blob. Core. Windows. net/{Kapsayıcıadı}" depolama kapsayıcısının "mhsm-myHsm-2020101308504935" adlı klasörde depolanan bir yedeklemeyi geri yükler.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="fa9c9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa9c9-115">PARAMETERS</span></span>

### <span data-ttu-id="fa9c9-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="fa9c9-116">-BackupFolder</span></span>
<span data-ttu-id="fa9c9-117">Yedeğin klasör adı, örneğin ' mhsm- *-2020101309020403 '. Ayrıca, ' yedekler/mhsm--2020101309020403 ' gibi iç içe geçmiş olabilir*.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9c9-118">-DefaultProfile</span></span>
<span data-ttu-id="fa9c9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="fa9c9-120">-HsmObject</span></span>
<span data-ttu-id="fa9c9-121">Yönetilen HSM nesnesi</span><span class="sxs-lookup"><span data-stu-id="fa9c9-121">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa9c9-122">-Name</span></span>
<span data-ttu-id="fa9c9-123">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fa9c9-124">-PassThru</span></span>
<span data-ttu-id="fa9c9-125">HSM geri yüklendiğinde doğru döner.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-125">Return true when the HSM is restored.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="fa9c9-126">-SasToken</span></span>
<span data-ttu-id="fa9c9-127">Depolama hesabının kimliğini doğrulamak için paylaşılan erişim imzası (SAS) simgesi.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fa9c9-128">-StorageAccountName</span></span>
<span data-ttu-id="fa9c9-129">Yedeklemenin depolanacağı depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-129">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="fa9c9-130">-StorageContainerName</span></span>
<span data-ttu-id="fa9c9-131">Yedeklemenin depolanacağı blob kapsayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-131">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="fa9c9-132">-StorageContainerUri</span></span>
<span data-ttu-id="fa9c9-133">Yedeklemenin depolanacağı depolama kapsayıcısının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-133">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa9c9-134">-Confirm</span></span>
<span data-ttu-id="fa9c9-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9c9-136">-WhatIf</span></span>
<span data-ttu-id="fa9c9-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9c9-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9c9-139">CommonParameters</span></span>
<span data-ttu-id="fa9c9-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9c9-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fa9c9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9c9-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa9c9-142">INPUTS</span></span>

### <span data-ttu-id="fa9c9-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fa9c9-143">None</span></span>

## <span data-ttu-id="fa9c9-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa9c9-144">OUTPUTS</span></span>

### <span data-ttu-id="fa9c9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa9c9-145">System.Boolean</span></span>

## <span data-ttu-id="fa9c9-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa9c9-146">NOTES</span></span>

## <span data-ttu-id="fa9c9-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa9c9-147">RELATED LINKS</span></span>
