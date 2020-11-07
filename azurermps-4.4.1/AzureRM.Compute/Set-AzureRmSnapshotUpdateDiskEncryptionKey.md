---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 31f0312e2afe82adc1f7e3906b7efa312192585a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593581"
---
# <span data-ttu-id="4e975-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4e975-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="4e975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e975-102">SYNOPSIS</span></span>
<span data-ttu-id="4e975-103">Anlık görüntü güncelleştirme nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4e975-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e975-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e975-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e975-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e975-105">DESCRIPTION</span></span>
<span data-ttu-id="4e975-106">**Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet 'i, anlık görüntü güncelleştirme nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4e975-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="4e975-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e975-107">EXAMPLES</span></span>

### <span data-ttu-id="4e975-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4e975-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="4e975-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4e975-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4e975-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="4e975-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4e975-111">İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4e975-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="4e975-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e975-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4e975-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e975-113">PARAMETERS</span></span>

### <span data-ttu-id="4e975-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e975-114">-DefaultProfile</span></span>
<span data-ttu-id="4e975-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e975-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e975-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="4e975-116">-SecretUrl</span></span>
<span data-ttu-id="4e975-117">Gizli URL 'Yi belirtimi.</span><span class="sxs-lookup"><span data-stu-id="4e975-117">Specifes the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e975-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="4e975-118">-SnapshotUpdate</span></span>
<span data-ttu-id="4e975-119">Yerel anlık görüntü güncelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e975-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e975-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4e975-120">-SourceVaultId</span></span>
<span data-ttu-id="4e975-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e975-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e975-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e975-122">-Confirm</span></span>
<span data-ttu-id="4e975-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e975-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e975-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e975-124">-WhatIf</span></span>
<span data-ttu-id="4e975-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e975-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e975-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e975-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e975-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e975-127">CommonParameters</span></span>
<span data-ttu-id="4e975-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e975-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e975-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e975-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e975-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e975-130">INPUTS</span></span>

### <span data-ttu-id="4e975-131">Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="4e975-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="4e975-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4e975-132">System.String</span></span>

## <span data-ttu-id="4e975-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e975-133">OUTPUTS</span></span>

### <span data-ttu-id="4e975-134">Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="4e975-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="4e975-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e975-135">NOTES</span></span>

## <span data-ttu-id="4e975-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e975-136">RELATED LINKS</span></span>
