---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 382bbb84a12834ea35bf42d2a1cce95afa5d93de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752640"
---
# <span data-ttu-id="ca5c5-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="ca5c5-101">Update-AzDisk</span></span>

## <span data-ttu-id="ca5c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca5c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5c5-103">Bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-103">Updates a disk.</span></span>

## <span data-ttu-id="ca5c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca5c5-104">SYNTAX</span></span>

### <span data-ttu-id="ca5c5-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca5c5-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca5c5-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="ca5c5-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca5c5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca5c5-107">DESCRIPTION</span></span>
<span data-ttu-id="ca5c5-108">**Update-AzDisk** cmdlet 'i bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="ca5c5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca5c5-109">EXAMPLES</span></span>

### <span data-ttu-id="ca5c5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca5c5-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="ca5c5-111">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ca5c5-112">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ca5c5-113">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ca5c5-114">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ca5c5-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ca5c5-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="ca5c5-116">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="ca5c5-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ca5c5-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="ca5c5-118">Bu komutlar, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna de güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ca5c5-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca5c5-119">PARAMETERS</span></span>

### <span data-ttu-id="ca5c5-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="ca5c5-120">-AsJob</span></span>
<span data-ttu-id="ca5c5-121">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ca5c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5c5-122">-DefaultProfile</span></span>
<span data-ttu-id="ca5c5-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca5c5-124">-Disk</span><span class="sxs-lookup"><span data-stu-id="ca5c5-124">-Disk</span></span>
<span data-ttu-id="ca5c5-125">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5c5-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ca5c5-126">-DiskName</span></span>
<span data-ttu-id="ca5c5-127">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-127">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5c5-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ca5c5-128">-DiskUpdate</span></span>
<span data-ttu-id="ca5c5-129">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="ca5c5-131">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-131">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5c5-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca5c5-132">-Confirm</span></span>
<span data-ttu-id="ca5c5-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca5c5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5c5-134">-WhatIf</span></span>
<span data-ttu-id="ca5c5-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca5c5-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca5c5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5c5-137">CommonParameters</span></span>
<span data-ttu-id="ca5c5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5c5-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca5c5-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5c5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca5c5-140">INPUTS</span></span>

### <span data-ttu-id="ca5c5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ca5c5-141">System.String</span></span>

### <span data-ttu-id="ca5c5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="ca5c5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="ca5c5-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="ca5c5-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ca5c5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca5c5-144">OUTPUTS</span></span>

### <span data-ttu-id="ca5c5-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="ca5c5-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ca5c5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca5c5-146">NOTES</span></span>

## <span data-ttu-id="ca5c5-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca5c5-147">RELATED LINKS</span></span>