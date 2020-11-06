---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4d44bc014a3d38a89e6c9a6a6d755aa9353c052e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591704"
---
# <span data-ttu-id="311c5-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="311c5-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="311c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="311c5-102">SYNOPSIS</span></span>
<span data-ttu-id="311c5-103">Disk güncelleştirme nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="311c5-103">Sets the disk encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="311c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="311c5-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateDiskEncryptionKey [-DiskUpdate] <DiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="311c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="311c5-105">DESCRIPTION</span></span>
<span data-ttu-id="311c5-106">**Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet 'i, disk güncelleştirme nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="311c5-106">The **Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="311c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="311c5-107">EXAMPLES</span></span>

### <span data-ttu-id="311c5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="311c5-108">Example 1</span></span>
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

<span data-ttu-id="311c5-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="311c5-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="311c5-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="311c5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="311c5-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="311c5-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="311c5-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="311c5-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="311c5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="311c5-113">PARAMETERS</span></span>

### <span data-ttu-id="311c5-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="311c5-114">-DiskUpdate</span></span>
<span data-ttu-id="311c5-115">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="311c5-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="311c5-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="311c5-116">-SecretUrl</span></span>
<span data-ttu-id="311c5-117">Gizli URL 'Yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="311c5-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="311c5-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="311c5-118">-SourceVaultId</span></span>
<span data-ttu-id="311c5-119">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="311c5-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="311c5-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="311c5-120">-Confirm</span></span>
<span data-ttu-id="311c5-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="311c5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="311c5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="311c5-122">-WhatIf</span></span>
<span data-ttu-id="311c5-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="311c5-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="311c5-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="311c5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="311c5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311c5-125">CommonParameters</span></span>
<span data-ttu-id="311c5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="311c5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311c5-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311c5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311c5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="311c5-128">INPUTS</span></span>

### <span data-ttu-id="311c5-129">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="311c5-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="311c5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="311c5-130">System.String</span></span>

## <span data-ttu-id="311c5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="311c5-131">OUTPUTS</span></span>

### <span data-ttu-id="311c5-132">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="311c5-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="311c5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="311c5-133">NOTES</span></span>

## <span data-ttu-id="311c5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="311c5-134">RELATED LINKS</span></span>

