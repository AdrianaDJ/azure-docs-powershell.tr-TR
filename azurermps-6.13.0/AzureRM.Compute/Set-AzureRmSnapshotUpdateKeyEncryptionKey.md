---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: fbd62d704bcbb3a73910d1c19db3698a09c6a90f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764676"
---
# <span data-ttu-id="d1b5b-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d1b5b-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="d1b5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b5b-103">Anlık görüntü güncelleştirme nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1b5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1b5b-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1b5b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1b5b-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b5b-106">**Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet 'i, anlık görüntü güncelleştirme nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="d1b5b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1b5b-107">EXAMPLES</span></span>

### <span data-ttu-id="d1b5b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d1b5b-108">Example 1</span></span>
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

<span data-ttu-id="d1b5b-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d1b5b-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d1b5b-111">İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="d1b5b-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d1b5b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1b5b-113">PARAMETERS</span></span>

### <span data-ttu-id="d1b5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b5b-114">-DefaultProfile</span></span>
<span data-ttu-id="d1b5b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1b5b-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="d1b5b-116">-KeyUrl</span></span>
<span data-ttu-id="d1b5b-117">Anahtar URL 'Yi belirtimi.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="d1b5b-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d1b5b-118">-SnapshotUpdate</span></span>
<span data-ttu-id="d1b5b-119">Yerel anlık görüntü güncelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="d1b5b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d1b5b-120">-SourceVaultId</span></span>
<span data-ttu-id="d1b5b-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="d1b5b-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1b5b-122">-Confirm</span></span>
<span data-ttu-id="d1b5b-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b5b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b5b-124">-WhatIf</span></span>
<span data-ttu-id="d1b5b-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1b5b-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b5b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b5b-127">CommonParameters</span></span>
<span data-ttu-id="d1b5b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1b5b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b5b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b5b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b5b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1b5b-130">INPUTS</span></span>

### <span data-ttu-id="d1b5b-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d1b5b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="d1b5b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d1b5b-132">System.String</span></span>

## <span data-ttu-id="d1b5b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1b5b-133">OUTPUTS</span></span>

### <span data-ttu-id="d1b5b-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d1b5b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="d1b5b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1b5b-135">NOTES</span></span>

## <span data-ttu-id="d1b5b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1b5b-136">RELATED LINKS</span></span>
