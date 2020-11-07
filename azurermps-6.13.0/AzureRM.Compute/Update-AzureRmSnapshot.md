---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: fba3ec6f6ab78042a9e597a1c1074626afcddb25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762983"
---
# <span data-ttu-id="b44e2-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b44e2-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="b44e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b44e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b44e2-103">Anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b44e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b44e2-104">SYNTAX</span></span>

### <span data-ttu-id="b44e2-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b44e2-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b44e2-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="b44e2-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b44e2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b44e2-107">DESCRIPTION</span></span>
<span data-ttu-id="b44e2-108">**Update-AzureRmSnapshot** cmdlet 'ini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="b44e2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b44e2-109">EXAMPLES</span></span>

### <span data-ttu-id="b44e2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b44e2-110">Example 1</span></span>
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

<span data-ttu-id="b44e2-111">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b44e2-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b44e2-112">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="b44e2-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b44e2-113">İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b44e2-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b44e2-114">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b44e2-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b44e2-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="b44e2-116">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="b44e2-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b44e2-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="b44e2-118">Bu komutlar, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna de güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b44e2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b44e2-119">PARAMETERS</span></span>

### <span data-ttu-id="b44e2-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="b44e2-120">-AsJob</span></span>
<span data-ttu-id="b44e2-121">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="b44e2-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44e2-122">-DefaultProfile</span></span>
<span data-ttu-id="b44e2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b44e2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b44e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b44e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b44e2-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b44e2-126">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="b44e2-126">-Snapshot</span></span>
<span data-ttu-id="b44e2-127">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b44e2-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b44e2-128">-SnapshotName</span></span>
<span data-ttu-id="b44e2-129">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b44e2-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b44e2-130">-SnapshotUpdate</span></span>
<span data-ttu-id="b44e2-131">Yerel anlık görüntü güncelleştirme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b44e2-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="b44e2-132">-Confirm</span></span>
<span data-ttu-id="b44e2-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b44e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b44e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b44e2-134">-WhatIf</span></span>
<span data-ttu-id="b44e2-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b44e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b44e2-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b44e2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b44e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44e2-137">CommonParameters</span></span>
<span data-ttu-id="b44e2-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b44e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44e2-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44e2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44e2-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b44e2-140">INPUTS</span></span>

### <span data-ttu-id="b44e2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b44e2-141">System.String</span></span>

### <span data-ttu-id="b44e2-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b44e2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>
<span data-ttu-id="b44e2-143">Parametreler: SnapshotUpdate (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b44e2-143">Parameters: SnapshotUpdate (ByValue)</span></span>

### <span data-ttu-id="b44e2-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b44e2-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>
<span data-ttu-id="b44e2-145">Parametreler: Snapshot (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b44e2-145">Parameters: Snapshot (ByValue)</span></span>

## <span data-ttu-id="b44e2-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b44e2-146">OUTPUTS</span></span>

### <span data-ttu-id="b44e2-147">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b44e2-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b44e2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b44e2-148">NOTES</span></span>

## <span data-ttu-id="b44e2-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b44e2-149">RELATED LINKS</span></span>