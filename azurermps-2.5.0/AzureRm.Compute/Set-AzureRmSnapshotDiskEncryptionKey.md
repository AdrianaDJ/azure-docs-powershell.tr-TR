---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotdiskencryptionkey
schema: 2.0.0
ms.openlocfilehash: f78b680f5872301236c5d001ce9920d2edd61f02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938981"
---
# <span data-ttu-id="6fc0b-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6fc0b-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="6fc0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fc0b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc0b-103">Anlık görüntü nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fc0b-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fc0b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fc0b-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc0b-106">**Set-AzureRmSnapshotDiskEncryptionKey** cmdlet 'i, anlık görüntü nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="6fc0b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fc0b-107">EXAMPLES</span></span>

### <span data-ttu-id="6fc0b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6fc0b-108">Example 1</span></span>
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

<span data-ttu-id="6fc0b-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="6fc0b-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6fc0b-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="6fc0b-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6fc0b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fc0b-113">PARAMETERS</span></span>

### <span data-ttu-id="6fc0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc0b-114">-DefaultProfile</span></span>
<span data-ttu-id="6fc0b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc0b-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="6fc0b-116">-SecretUrl</span></span>
<span data-ttu-id="6fc0b-117">Gizli URL 'Yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="6fc0b-118">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="6fc0b-118">-Snapshot</span></span>
<span data-ttu-id="6fc0b-119">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc0b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6fc0b-120">-SourceVaultId</span></span>
<span data-ttu-id="6fc0b-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="6fc0b-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fc0b-122">-Confirm</span></span>
<span data-ttu-id="6fc0b-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc0b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc0b-124">-WhatIf</span></span>
<span data-ttu-id="6fc0b-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fc0b-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc0b-127">CommonParameters</span></span>
<span data-ttu-id="6fc0b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fc0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc0b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc0b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc0b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fc0b-130">INPUTS</span></span>

### <span data-ttu-id="6fc0b-131">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="6fc0b-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="6fc0b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6fc0b-132">System.String</span></span>

## <span data-ttu-id="6fc0b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fc0b-133">OUTPUTS</span></span>

### <span data-ttu-id="6fc0b-134">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="6fc0b-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="6fc0b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fc0b-135">NOTES</span></span>

## <span data-ttu-id="6fc0b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fc0b-136">RELATED LINKS</span></span>

