---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 9c6debcae0aa83dd08374c7e390e3a42c4e5233a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586785"
---
# <span data-ttu-id="eb8b5-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="eb8b5-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="eb8b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8b5-103">Anlık görüntü nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb8b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb8b5-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <Snapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb8b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="eb8b5-106">**Set-AzureRmSnapshotKeyEncryptionKey** cmdlet 'i, anlık görüntü nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="eb8b5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb8b5-107">EXAMPLES</span></span>

### <span data-ttu-id="eb8b5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eb8b5-108">Example 1</span></span>
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

<span data-ttu-id="eb8b5-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="eb8b5-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="eb8b5-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="eb8b5-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="eb8b5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb8b5-113">PARAMETERS</span></span>

### <span data-ttu-id="eb8b5-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="eb8b5-114">-KeyUrl</span></span>
<span data-ttu-id="eb8b5-115">Anahtar URL 'Yi belirtimi.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-115">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b5-116">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="eb8b5-116">-Snapshot</span></span>
<span data-ttu-id="eb8b5-117">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b5-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="eb8b5-118">-SourceVaultId</span></span>
<span data-ttu-id="eb8b5-119">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b5-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb8b5-120">-Confirm</span></span>
<span data-ttu-id="eb8b5-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8b5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8b5-122">-WhatIf</span></span>
<span data-ttu-id="eb8b5-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb8b5-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8b5-125">CommonParameters</span></span>
<span data-ttu-id="eb8b5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb8b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8b5-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8b5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb8b5-128">INPUTS</span></span>

### <span data-ttu-id="eb8b5-129">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="eb8b5-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="eb8b5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eb8b5-130">System.String</span></span>

## <span data-ttu-id="eb8b5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb8b5-131">OUTPUTS</span></span>

### <span data-ttu-id="eb8b5-132">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="eb8b5-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="eb8b5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb8b5-133">NOTES</span></span>

## <span data-ttu-id="eb8b5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb8b5-134">RELATED LINKS</span></span>

