---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskKeyEncryptionKey.md
ms.openlocfilehash: bcefac746d643bfa64b28c623292e6473f8a4986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591705"
---
# <span data-ttu-id="d5490-101">Set-AzureRmDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d5490-101">Set-AzureRmDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="d5490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5490-102">SYNOPSIS</span></span>
<span data-ttu-id="d5490-103">Disk nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d5490-103">Sets the key encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5490-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5490-104">SYNTAX</span></span>

```
Set-AzureRmDiskKeyEncryptionKey [-Disk] <Disk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5490-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5490-105">DESCRIPTION</span></span>
<span data-ttu-id="d5490-106">**Set-AzureRmDiskKeyEncryptionKey** cmdlet 'i, disk nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d5490-106">The **Set-AzureRmDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="d5490-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5490-107">EXAMPLES</span></span>

### <span data-ttu-id="d5490-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5490-108">Example 1</span></span>
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

<span data-ttu-id="d5490-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5490-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d5490-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="d5490-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d5490-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d5490-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="d5490-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5490-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d5490-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5490-113">PARAMETERS</span></span>

### <span data-ttu-id="d5490-114">-Disk</span><span class="sxs-lookup"><span data-stu-id="d5490-114">-Disk</span></span>
<span data-ttu-id="d5490-115">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5490-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5490-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="d5490-116">-KeyUrl</span></span>
<span data-ttu-id="d5490-117">Anahtar URL 'Yi belirtimi.</span><span class="sxs-lookup"><span data-stu-id="d5490-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="d5490-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d5490-118">-SourceVaultId</span></span>
<span data-ttu-id="d5490-119">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5490-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="d5490-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5490-120">-Confirm</span></span>
<span data-ttu-id="d5490-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5490-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5490-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5490-122">-WhatIf</span></span>
<span data-ttu-id="d5490-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5490-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5490-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5490-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5490-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5490-125">CommonParameters</span></span>
<span data-ttu-id="d5490-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5490-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5490-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5490-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5490-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5490-128">INPUTS</span></span>

### <span data-ttu-id="d5490-129">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="d5490-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="d5490-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d5490-130">System.String</span></span>

## <span data-ttu-id="d5490-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5490-131">OUTPUTS</span></span>

### <span data-ttu-id="d5490-132">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="d5490-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="d5490-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5490-133">NOTES</span></span>

## <span data-ttu-id="d5490-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5490-134">RELATED LINKS</span></span>

