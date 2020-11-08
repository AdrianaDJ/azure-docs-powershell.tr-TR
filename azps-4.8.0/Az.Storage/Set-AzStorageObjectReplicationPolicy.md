---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267532"
---
# <span data-ttu-id="35f0e-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="35f0e-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="35f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="35f0e-103">Bir depolama hesabında belirtilen nesne çoğaltma ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="35f0e-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="35f0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35f0e-104">SYNTAX</span></span>

### <span data-ttu-id="35f0e-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35f0e-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35f0e-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="35f0e-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35f0e-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="35f0e-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f0e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="35f0e-108">DESCRIPTION</span></span>
<span data-ttu-id="35f0e-109">**Set-AzStorageObjectReplicationPolicy** cmdlet 'i, bir depolama hesabında belirtilen nesne çoğaltma ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="35f0e-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="35f0e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35f0e-110">EXAMPLES</span></span>

### <span data-ttu-id="35f0e-111">Örnek 1: nesne çoğaltma ilkesini hem hedef hem de kaynak hesaba ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="35f0e-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="35f0e-112">Bu komut, nesne çoğaltma ilkesini hem hedef hem de kaynak hesaba ayarlar.</span><span class="sxs-lookup"><span data-stu-id="35f0e-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="35f0e-113">İlk önce 2 nesne çoğaltma ilkesi kuralı oluşturun ve kuralı hedef hesapla 2 kuralla ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="35f0e-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="35f0e-114">Ardından, nesne çoğaltma ilkesini hedef hesaptan kaynak hesaba ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="35f0e-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="35f0e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35f0e-115">PARAMETERS</span></span>

### <span data-ttu-id="35f0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f0e-116">-DefaultProfile</span></span>
<span data-ttu-id="35f0e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35f0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="35f0e-118">-DestinationAccount</span></span>
<span data-ttu-id="35f0e-119">Nesne çoğaltma Ilkesi DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="35f0e-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35f0e-120">-InputObject</span></span>
<span data-ttu-id="35f0e-121">Belirtilen hesaba ayarlanacak nesne çoğaltma Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="35f0e-121">Object Replication Policy Object to Set to the specified Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="35f0e-122">-PolicyId</span></span>
<span data-ttu-id="35f0e-123">Nesne çoğaltma Ilkesi kimliği. GUID veya ' default ' olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35f0e-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="35f0e-124">PolicyId 'nin girişi yoksa, yeni ilke oluşturmak ve oluşturulan ilkede yeni ilkenin kimliği geri döndürülürsünüz.</span><span class="sxs-lookup"><span data-stu-id="35f0e-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f0e-125">-ResourceGroupName</span></span>
<span data-ttu-id="35f0e-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="35f0e-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-127">-Kural</span><span class="sxs-lookup"><span data-stu-id="35f0e-127">-Rule</span></span>
<span data-ttu-id="35f0e-128">Nesne çoğaltma Ilkesi kuralları.</span><span class="sxs-lookup"><span data-stu-id="35f0e-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="35f0e-129">-SourceAccount</span></span>
<span data-ttu-id="35f0e-130">Nesne çoğaltma Ilkesi SourceAccount.</span><span class="sxs-lookup"><span data-stu-id="35f0e-130">Object Replication Policy SourceAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="35f0e-131">-StorageAccount</span></span>
<span data-ttu-id="35f0e-132">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="35f0e-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35f0e-133">-StorageAccountName</span></span>
<span data-ttu-id="35f0e-134">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="35f0e-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f0e-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="35f0e-135">-Confirm</span></span>
<span data-ttu-id="35f0e-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35f0e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f0e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f0e-137">-WhatIf</span></span>
<span data-ttu-id="35f0e-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35f0e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f0e-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35f0e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f0e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f0e-140">CommonParameters</span></span>
<span data-ttu-id="35f0e-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35f0e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f0e-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f0e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f0e-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35f0e-143">INPUTS</span></span>

### <span data-ttu-id="35f0e-144">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35f0e-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="35f0e-145">Microsoft. Azure. Commands. Management. Storage. model. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="35f0e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="35f0e-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35f0e-146">OUTPUTS</span></span>

### <span data-ttu-id="35f0e-147">Microsoft. Azure. Commands. Management. Storage. model. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="35f0e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="35f0e-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35f0e-148">NOTES</span></span>

## <span data-ttu-id="35f0e-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35f0e-149">RELATED LINKS</span></span>
