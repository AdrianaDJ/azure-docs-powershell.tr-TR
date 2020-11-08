---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268720"
---
# <span data-ttu-id="92545-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="92545-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="92545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92545-102">SYNOPSIS</span></span>
<span data-ttu-id="92545-103">SQL yönetilen örneğinin işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="92545-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="92545-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92545-104">SYNTAX</span></span>

### <span data-ttu-id="92545-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="92545-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92545-106">Getbymanagedınstanceoperationresourceıdentifierparameterset</span><span class="sxs-lookup"><span data-stu-id="92545-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92545-107">Listbymanagedınstanceparameterset</span><span class="sxs-lookup"><span data-stu-id="92545-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92545-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="92545-108">DESCRIPTION</span></span>
<span data-ttu-id="92545-109">Get-AzSqlInstanceOperation cmdlet 'i SQL yönetilen örneğindeki işlemler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="92545-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="92545-110">Yönetilen bir örnekteki tüm işlemleri görüntüleyebilir veya işlem adını sağlayarak belirli bir işlemi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92545-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="92545-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92545-111">EXAMPLES</span></span>

### <span data-ttu-id="92545-112">Örnek 1: tüm örneğin işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="92545-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="92545-113">Bu komut tüm işlemleri bir SQL yönetilen örneğine alır.</span><span class="sxs-lookup"><span data-stu-id="92545-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="92545-114">Örnek 2: belirli bir işlem edinme</span><span class="sxs-lookup"><span data-stu-id="92545-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="92545-115">Bu komut, SQL yönetilen örneğindeki ' 5870c6vseç8-6703-4b27-8AE4-687b4ca7caea ' adlı işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="92545-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="92545-116">Örnek 3: işlem kaynak kimliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="92545-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="92545-117">Bu komut '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea ' kimliğine sahip işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="92545-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="92545-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92545-118">PARAMETERS</span></span>

### <span data-ttu-id="92545-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92545-119">-DefaultProfile</span></span>
<span data-ttu-id="92545-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92545-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92545-121">-Managedınstancename</span><span class="sxs-lookup"><span data-stu-id="92545-121">-ManagedInstanceName</span></span>
<span data-ttu-id="92545-122">Örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="92545-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92545-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="92545-123">-Name</span></span>
<span data-ttu-id="92545-124">İşlemin adı.</span><span class="sxs-lookup"><span data-stu-id="92545-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92545-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92545-125">-ResourceGroupName</span></span>
<span data-ttu-id="92545-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="92545-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92545-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="92545-127">-ResourceId</span></span>
<span data-ttu-id="92545-128">Yönetilen örnek işlemi kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="92545-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92545-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92545-129">CommonParameters</span></span>
<span data-ttu-id="92545-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92545-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92545-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="92545-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92545-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92545-132">INPUTS</span></span>

### <span data-ttu-id="92545-133">System. String</span><span class="sxs-lookup"><span data-stu-id="92545-133">System.String</span></span>

## <span data-ttu-id="92545-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92545-134">OUTPUTS</span></span>

### <span data-ttu-id="92545-135">Microsoft. Azure. Commands. Sql. Managedınstanceoperation. model. Azurestabmanagedınstanceoperationmodel</span><span class="sxs-lookup"><span data-stu-id="92545-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="92545-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92545-136">NOTES</span></span>

## <span data-ttu-id="92545-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92545-137">RELATED LINKS</span></span>
