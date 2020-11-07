---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 81cf8a6d011575702f8eead878e8987a5a0fd456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764891"
---
# <span data-ttu-id="38d14-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="38d14-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="38d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d14-102">SYNOPSIS</span></span>
<span data-ttu-id="38d14-103">Bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38d14-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38d14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38d14-104">SYNTAX</span></span>

### <span data-ttu-id="38d14-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38d14-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38d14-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="38d14-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d14-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="38d14-107">DESCRIPTION</span></span>
<span data-ttu-id="38d14-108">**Güncelleştirme-AzureRmDisk** cmdlet 'i bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38d14-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="38d14-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38d14-109">EXAMPLES</span></span>

### <span data-ttu-id="38d14-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="38d14-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="38d14-111">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38d14-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="38d14-112">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="38d14-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="38d14-113">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="38d14-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="38d14-114">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38d14-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="38d14-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="38d14-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="38d14-116">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38d14-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="38d14-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="38d14-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="38d14-118">Bu komutlar, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna de güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38d14-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="38d14-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38d14-119">PARAMETERS</span></span>

### <span data-ttu-id="38d14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d14-120">-DefaultProfile</span></span>
<span data-ttu-id="38d14-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38d14-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d14-122">-Disk</span><span class="sxs-lookup"><span data-stu-id="38d14-122">-Disk</span></span>
<span data-ttu-id="38d14-123">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38d14-123">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38d14-124">-DiskName</span><span class="sxs-lookup"><span data-stu-id="38d14-124">-DiskName</span></span>
<span data-ttu-id="38d14-125">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38d14-125">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d14-126">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="38d14-126">-DiskUpdate</span></span>
<span data-ttu-id="38d14-127">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="38d14-127">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38d14-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d14-128">-ResourceGroupName</span></span>
<span data-ttu-id="38d14-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38d14-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d14-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="38d14-130">-Confirm</span></span>
<span data-ttu-id="38d14-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38d14-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d14-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d14-132">-WhatIf</span></span>
<span data-ttu-id="38d14-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38d14-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d14-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38d14-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d14-135">CommonParameters</span></span>
<span data-ttu-id="38d14-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38d14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d14-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d14-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d14-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38d14-138">INPUTS</span></span>

### <span data-ttu-id="38d14-139">System. String</span><span class="sxs-lookup"><span data-stu-id="38d14-139">System.String</span></span>
<span data-ttu-id="38d14-140">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="38d14-140">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="38d14-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38d14-141">OUTPUTS</span></span>

### <span data-ttu-id="38d14-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="38d14-142">System.Object</span></span>

## <span data-ttu-id="38d14-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38d14-143">NOTES</span></span>

## <span data-ttu-id="38d14-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38d14-144">RELATED LINKS</span></span>

