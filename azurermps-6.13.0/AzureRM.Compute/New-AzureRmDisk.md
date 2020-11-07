---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: e73b1a316402722e03ff9c26fd27610cb916b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763005"
---
# <span data-ttu-id="c58be-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c58be-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="c58be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c58be-102">SYNOPSIS</span></span>
<span data-ttu-id="c58be-103">Yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c58be-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c58be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c58be-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c58be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c58be-105">DESCRIPTION</span></span>
<span data-ttu-id="c58be-106">**Yeni-AzureRmDisk** cmdlet 'i yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c58be-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="c58be-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c58be-107">EXAMPLES</span></span>

### <span data-ttu-id="c58be-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c58be-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="c58be-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c58be-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="c58be-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="c58be-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c58be-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c58be-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="c58be-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c58be-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c58be-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c58be-113">PARAMETERS</span></span>

### <span data-ttu-id="c58be-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="c58be-114">-AsJob</span></span>
<span data-ttu-id="c58be-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="c58be-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c58be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c58be-116">-DefaultProfile</span></span>
<span data-ttu-id="c58be-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c58be-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c58be-118">-Disk</span><span class="sxs-lookup"><span data-stu-id="c58be-118">-Disk</span></span>
<span data-ttu-id="c58be-119">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c58be-119">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c58be-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c58be-120">-DiskName</span></span>
<span data-ttu-id="c58be-121">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c58be-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c58be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c58be-122">-ResourceGroupName</span></span>
<span data-ttu-id="c58be-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c58be-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c58be-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="c58be-124">-Confirm</span></span>
<span data-ttu-id="c58be-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c58be-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c58be-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c58be-126">-WhatIf</span></span>
<span data-ttu-id="c58be-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c58be-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c58be-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c58be-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c58be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58be-129">CommonParameters</span></span>
<span data-ttu-id="c58be-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c58be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58be-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c58be-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58be-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c58be-132">INPUTS</span></span>

### <span data-ttu-id="c58be-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c58be-133">System.String</span></span>

### <span data-ttu-id="c58be-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="c58be-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>
<span data-ttu-id="c58be-135">Parametreler: disk (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c58be-135">Parameters: Disk (ByValue)</span></span>

## <span data-ttu-id="c58be-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c58be-136">OUTPUTS</span></span>

### <span data-ttu-id="c58be-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="c58be-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="c58be-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c58be-138">NOTES</span></span>

## <span data-ttu-id="c58be-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c58be-139">RELATED LINKS</span></span>
