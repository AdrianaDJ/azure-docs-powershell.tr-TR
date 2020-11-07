---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: fa77808eddc0e51fa76a0883980b34552589f4ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939793"
---
# <span data-ttu-id="c39b0-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c39b0-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="c39b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c39b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c39b0-103">Anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39b0-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c39b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c39b0-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c39b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c39b0-105">DESCRIPTION</span></span>
<span data-ttu-id="c39b0-106">**Yeni-AzureRmSnapshot** cmdlet 'i anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39b0-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="c39b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c39b0-107">EXAMPLES</span></span>

### <span data-ttu-id="c39b0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c39b0-108">Example 1</span></span>
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

<span data-ttu-id="c39b0-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39b0-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="c39b0-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="c39b0-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c39b0-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c39b0-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="c39b0-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39b0-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c39b0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c39b0-113">PARAMETERS</span></span>

### <span data-ttu-id="c39b0-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="c39b0-114">-AsJob</span></span>
<span data-ttu-id="c39b0-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="c39b0-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39b0-116">-DefaultProfile</span></span>
<span data-ttu-id="c39b0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c39b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c39b0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39b0-118">-ResourceGroupName</span></span>
<span data-ttu-id="c39b0-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c39b0-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c39b0-120">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="c39b0-120">-Snapshot</span></span>
<span data-ttu-id="c39b0-121">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c39b0-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c39b0-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c39b0-122">-SnapshotName</span></span>
<span data-ttu-id="c39b0-123">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c39b0-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c39b0-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="c39b0-124">-Confirm</span></span>
<span data-ttu-id="c39b0-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c39b0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c39b0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39b0-126">-WhatIf</span></span>
<span data-ttu-id="c39b0-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c39b0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39b0-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c39b0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c39b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39b0-129">CommonParameters</span></span>
<span data-ttu-id="c39b0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c39b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39b0-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c39b0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39b0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c39b0-132">INPUTS</span></span>

### <span data-ttu-id="c39b0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c39b0-133">System.String</span></span>
<span data-ttu-id="c39b0-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="c39b0-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="c39b0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c39b0-135">OUTPUTS</span></span>

### <span data-ttu-id="c39b0-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="c39b0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="c39b0-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="c39b0-137">System.Object</span></span>

## <span data-ttu-id="c39b0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c39b0-138">NOTES</span></span>

## <span data-ttu-id="c39b0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c39b0-139">RELATED LINKS</span></span>

