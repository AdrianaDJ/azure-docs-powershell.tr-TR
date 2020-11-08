---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266260"
---
# <span data-ttu-id="dae92-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="dae92-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="dae92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dae92-102">SYNOPSIS</span></span>
<span data-ttu-id="dae92-103">Depolama hesabının nesne çoğaltma ilkesini alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="dae92-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="dae92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dae92-104">SYNTAX</span></span>

### <span data-ttu-id="dae92-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dae92-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dae92-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="dae92-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dae92-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dae92-107">DESCRIPTION</span></span>
<span data-ttu-id="dae92-108">**Get-AzStorageObjectReplicationPolicy** cmdlet 'ı bir depolama hesabının nesne çoğaltma ilkesini alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="dae92-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="dae92-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dae92-109">EXAMPLES</span></span>

### <span data-ttu-id="dae92-110">Örnek 1: belirli ilke kimliğine sahip bir nesne çoğaltma ilkesi alın ve kurallarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="dae92-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="dae92-111">Bu komut, belirli bir ilke kimliğiyle nesne çoğaltma ilkesi alır ve kurallarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dae92-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="dae92-112">Örnek 2: depolama hesabından liste nesnesi çoğaltma ilkesi</span><span class="sxs-lookup"><span data-stu-id="dae92-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="dae92-113">Bu komut, depolama hesabındaki nesne çoğaltma ilkesini listeler.</span><span class="sxs-lookup"><span data-stu-id="dae92-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="dae92-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dae92-114">PARAMETERS</span></span>

### <span data-ttu-id="dae92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae92-115">-DefaultProfile</span></span>
<span data-ttu-id="dae92-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dae92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae92-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="dae92-117">-PolicyId</span></span>
<span data-ttu-id="dae92-118">Nesne çoğaltma Ilkesi kimliği.</span><span class="sxs-lookup"><span data-stu-id="dae92-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae92-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae92-119">-ResourceGroupName</span></span>
<span data-ttu-id="dae92-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dae92-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae92-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="dae92-121">-StorageAccount</span></span>
<span data-ttu-id="dae92-122">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="dae92-122">Storage account object</span></span>

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

### <span data-ttu-id="dae92-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dae92-123">-StorageAccountName</span></span>
<span data-ttu-id="dae92-124">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="dae92-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae92-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae92-125">CommonParameters</span></span>
<span data-ttu-id="dae92-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dae92-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae92-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae92-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae92-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dae92-128">INPUTS</span></span>

### <span data-ttu-id="dae92-129">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dae92-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dae92-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dae92-130">OUTPUTS</span></span>

### <span data-ttu-id="dae92-131">Microsoft. Azure. Commands. Management. Storage. model. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="dae92-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="dae92-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dae92-132">NOTES</span></span>

## <span data-ttu-id="dae92-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dae92-133">RELATED LINKS</span></span>
