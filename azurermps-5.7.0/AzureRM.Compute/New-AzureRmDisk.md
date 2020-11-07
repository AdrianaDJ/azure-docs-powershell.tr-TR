---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 04106c91e99372b985c0a10ac12a7944fdcb4e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764471"
---
# <span data-ttu-id="cef8b-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="cef8b-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="cef8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef8b-102">SYNOPSIS</span></span>
<span data-ttu-id="cef8b-103">Yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cef8b-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cef8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cef8b-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cef8b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cef8b-105">DESCRIPTION</span></span>
<span data-ttu-id="cef8b-106">**Yeni-AzureRmDisk** cmdlet 'i yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cef8b-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="cef8b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cef8b-107">EXAMPLES</span></span>

### <span data-ttu-id="cef8b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cef8b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="cef8b-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cef8b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="cef8b-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="cef8b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cef8b-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cef8b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="cef8b-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cef8b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cef8b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cef8b-113">PARAMETERS</span></span>

### <span data-ttu-id="cef8b-114">-Disk</span><span class="sxs-lookup"><span data-stu-id="cef8b-114">-Disk</span></span>
<span data-ttu-id="cef8b-115">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cef8b-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef8b-116">-DiskName</span><span class="sxs-lookup"><span data-stu-id="cef8b-116">-DiskName</span></span>
<span data-ttu-id="cef8b-117">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cef8b-117">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef8b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef8b-118">-ResourceGroupName</span></span>
<span data-ttu-id="cef8b-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cef8b-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef8b-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="cef8b-120">-Confirm</span></span>
<span data-ttu-id="cef8b-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cef8b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef8b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef8b-122">-WhatIf</span></span>
<span data-ttu-id="cef8b-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cef8b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef8b-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cef8b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef8b-125">CommonParameters</span></span>
<span data-ttu-id="cef8b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cef8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef8b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef8b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef8b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cef8b-128">INPUTS</span></span>

### <span data-ttu-id="cef8b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cef8b-129">System.String</span></span>
<span data-ttu-id="cef8b-130">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="cef8b-130">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="cef8b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cef8b-131">OUTPUTS</span></span>

### <span data-ttu-id="cef8b-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="cef8b-132">System.Object</span></span>

## <span data-ttu-id="cef8b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cef8b-133">NOTES</span></span>

## <span data-ttu-id="cef8b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cef8b-134">RELATED LINKS</span></span>

