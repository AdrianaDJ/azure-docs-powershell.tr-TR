---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275320"
---
# <span data-ttu-id="07f01-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="07f01-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="07f01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f01-102">SYNOPSIS</span></span>
<span data-ttu-id="07f01-103">Yönetilen bir HSM 'yi tümüyle yedekleme.</span><span class="sxs-lookup"><span data-stu-id="07f01-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="07f01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07f01-104">SYNTAX</span></span>

### <span data-ttu-id="07f01-105">InteractiveStorageName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07f01-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f01-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="07f01-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f01-107">Inputobjectstorageuri</span><span class="sxs-lookup"><span data-stu-id="07f01-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f01-108">Inputobjectstoragename</span><span class="sxs-lookup"><span data-stu-id="07f01-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f01-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="07f01-109">DESCRIPTION</span></span>
<span data-ttu-id="07f01-110">Yönetilen bir HSM 'yi depolama hesabına tam olarak yedekleme.</span><span class="sxs-lookup"><span data-stu-id="07f01-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="07f01-111">`Restore-AzManagedHsm`Yedeği geri yüklemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="07f01-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="07f01-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07f01-112">EXAMPLES</span></span>

### <span data-ttu-id="07f01-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07f01-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="07f01-114">Cmdlet, depolama kapsayıcısında bir klasör (genellikle adı `mhsm-{name}-{timestamp}` ) oluşturur, yedeği bu klasörde depolar ve klasör URI 'sini çıktısını alır.</span><span class="sxs-lookup"><span data-stu-id="07f01-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="07f01-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07f01-115">PARAMETERS</span></span>

### <span data-ttu-id="07f01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f01-116">-DefaultProfile</span></span>
<span data-ttu-id="07f01-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07f01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f01-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="07f01-118">-HsmObject</span></span>
<span data-ttu-id="07f01-119">Yönetilen HSM nesnesi</span><span class="sxs-lookup"><span data-stu-id="07f01-119">Managed HSM object</span></span>

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

### <span data-ttu-id="07f01-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="07f01-120">-Name</span></span>
<span data-ttu-id="07f01-121">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="07f01-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="07f01-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="07f01-122">-SasToken</span></span>
<span data-ttu-id="07f01-123">Depolama hesabının kimliğini doğrulamak için paylaşılan erişim imzası (SAS) simgesi.</span><span class="sxs-lookup"><span data-stu-id="07f01-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="07f01-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="07f01-124">-StorageAccountName</span></span>
<span data-ttu-id="07f01-125">Yedeklemenin depolanacağı depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="07f01-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="07f01-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="07f01-126">-StorageContainerName</span></span>
<span data-ttu-id="07f01-127">Yedeklemenin depolanacağı blob kapsayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="07f01-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="07f01-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="07f01-128">-StorageContainerUri</span></span>
<span data-ttu-id="07f01-129">Yedeklemenin depolanacağı depolama kapsayıcısının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="07f01-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="07f01-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="07f01-130">-Confirm</span></span>
<span data-ttu-id="07f01-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07f01-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f01-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f01-132">-WhatIf</span></span>
<span data-ttu-id="07f01-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07f01-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f01-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07f01-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f01-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f01-135">CommonParameters</span></span>
<span data-ttu-id="07f01-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07f01-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f01-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07f01-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f01-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07f01-138">INPUTS</span></span>

### <span data-ttu-id="07f01-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="07f01-139">None</span></span>

## <span data-ttu-id="07f01-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07f01-140">OUTPUTS</span></span>

### <span data-ttu-id="07f01-141">System. String</span><span class="sxs-lookup"><span data-stu-id="07f01-141">System.String</span></span>

## <span data-ttu-id="07f01-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07f01-142">NOTES</span></span>

## <span data-ttu-id="07f01-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07f01-143">RELATED LINKS</span></span>
