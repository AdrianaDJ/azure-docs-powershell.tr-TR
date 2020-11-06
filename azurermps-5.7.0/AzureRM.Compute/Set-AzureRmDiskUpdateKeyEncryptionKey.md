---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 3e1667cb7a8e8bd078e03d2ddafab559ca7b143f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591700"
---
# <span data-ttu-id="4f1ca-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4f1ca-101">Set-AzureRmDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="4f1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1ca-103">Disk güncelleştirme nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-103">Sets the key encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f1ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f1ca-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateKeyEncryptionKey [-DiskUpdate] <DiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="4f1ca-106">**Set-AzureRmDiskUpdateKeyEncryptionKey** cmdlet 'i, disk güncelleştirme nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-106">The **Set-AzureRmDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="4f1ca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="4f1ca-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f1ca-108">Example 1</span></span>
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

<span data-ttu-id="4f1ca-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4f1ca-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4f1ca-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="4f1ca-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4f1ca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f1ca-113">PARAMETERS</span></span>

### <span data-ttu-id="4f1ca-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="4f1ca-114">-DiskUpdate</span></span>
<span data-ttu-id="4f1ca-115">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-115">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="4f1ca-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="4f1ca-116">-KeyUrl</span></span>
<span data-ttu-id="4f1ca-117">Anahtar URL 'Yi belirtimi.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="4f1ca-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4f1ca-118">-SourceVaultId</span></span>
<span data-ttu-id="4f1ca-119">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="4f1ca-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f1ca-120">-Confirm</span></span>
<span data-ttu-id="4f1ca-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1ca-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f1ca-122">-WhatIf</span></span>
<span data-ttu-id="4f1ca-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f1ca-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1ca-125">CommonParameters</span></span>
<span data-ttu-id="4f1ca-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f1ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1ca-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f1ca-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1ca-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f1ca-128">INPUTS</span></span>

### <span data-ttu-id="4f1ca-129">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="4f1ca-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="4f1ca-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4f1ca-130">System.String</span></span>

## <span data-ttu-id="4f1ca-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f1ca-131">OUTPUTS</span></span>

### <span data-ttu-id="4f1ca-132">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="4f1ca-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="4f1ca-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f1ca-133">NOTES</span></span>

## <span data-ttu-id="4f1ca-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f1ca-134">RELATED LINKS</span></span>

