---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
ms.openlocfilehash: c7d88f16ff9eb6bb32cdf286ef37a1aba17030cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594792"
---
# <span data-ttu-id="5c1c8-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="5c1c8-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="5c1c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1c8-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1c8-103">Anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c1c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c1c8-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c1c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c1c8-105">DESCRIPTION</span></span>
<span data-ttu-id="5c1c8-106">**Yeni-AzureRmSnapshot** cmdlet 'i anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="5c1c8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c1c8-107">EXAMPLES</span></span>

### <span data-ttu-id="5c1c8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5c1c8-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="5c1c8-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="5c1c8-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5c1c8-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="5c1c8-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5c1c8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c1c8-113">PARAMETERS</span></span>

### <span data-ttu-id="5c1c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1c8-114">-DefaultProfile</span></span>
<span data-ttu-id="5c1c8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c1c8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1c8-116">-ResourceGroupName</span></span>
<span data-ttu-id="5c1c8-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5c1c8-118">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="5c1c8-118">-Snapshot</span></span>
<span data-ttu-id="5c1c8-119">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1c8-120">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5c1c8-120">-SnapshotName</span></span>
<span data-ttu-id="5c1c8-121">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-121">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5c1c8-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c1c8-122">-Confirm</span></span>
<span data-ttu-id="5c1c8-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1c8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1c8-124">-WhatIf</span></span>
<span data-ttu-id="5c1c8-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c1c8-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1c8-127">CommonParameters</span></span>
<span data-ttu-id="5c1c8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c1c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1c8-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1c8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1c8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c1c8-130">INPUTS</span></span>

### <span data-ttu-id="5c1c8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5c1c8-131">System.String</span></span>
<span data-ttu-id="5c1c8-132">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="5c1c8-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="5c1c8-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c1c8-133">OUTPUTS</span></span>

### <span data-ttu-id="5c1c8-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="5c1c8-134">System.Object</span></span>

## <span data-ttu-id="5c1c8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c1c8-135">NOTES</span></span>

## <span data-ttu-id="5c1c8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c1c8-136">RELATED LINKS</span></span>
