---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 4392c1ccf19474e1a8f73c5bccca2c09f53cbea8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765061"
---
# <span data-ttu-id="c87f5-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c87f5-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="c87f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c87f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c87f5-103">Yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c87f5-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c87f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c87f5-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c87f5-105">DESCRIPTION</span></span>
<span data-ttu-id="c87f5-106">**Yeni-AzureRmDisk** cmdlet 'i yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c87f5-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="c87f5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c87f5-107">EXAMPLES</span></span>

### <span data-ttu-id="c87f5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c87f5-108">Example 1</span></span>
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

<span data-ttu-id="c87f5-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c87f5-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="c87f5-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="c87f5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c87f5-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c87f5-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="c87f5-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c87f5-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c87f5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c87f5-113">PARAMETERS</span></span>

### <span data-ttu-id="c87f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87f5-114">-DefaultProfile</span></span>
<span data-ttu-id="c87f5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c87f5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c87f5-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="c87f5-116">-Disk</span></span>
<span data-ttu-id="c87f5-117">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87f5-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="c87f5-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="c87f5-118">-DiskName</span></span>
<span data-ttu-id="c87f5-119">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87f5-119">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c87f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c87f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="c87f5-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c87f5-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c87f5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="c87f5-122">-Confirm</span></span>
<span data-ttu-id="c87f5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c87f5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87f5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87f5-124">-WhatIf</span></span>
<span data-ttu-id="c87f5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c87f5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87f5-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c87f5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87f5-127">CommonParameters</span></span>
<span data-ttu-id="c87f5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c87f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87f5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87f5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87f5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c87f5-130">INPUTS</span></span>

### <span data-ttu-id="c87f5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c87f5-131">System.String</span></span>
<span data-ttu-id="c87f5-132">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="c87f5-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="c87f5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c87f5-133">OUTPUTS</span></span>

### <span data-ttu-id="c87f5-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="c87f5-134">System.Object</span></span>

## <span data-ttu-id="c87f5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c87f5-135">NOTES</span></span>

## <span data-ttu-id="c87f5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c87f5-136">RELATED LINKS</span></span>

