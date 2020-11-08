---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107541"
---
# <span data-ttu-id="6a3c6-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="6a3c6-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="6a3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3c6-103">SQL yönetilen örneğinin işlemlerini durdurur.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="6a3c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a3c6-104">SYNTAX</span></span>

### <span data-ttu-id="6a3c6-105">Stopbynaik Vseçmanagedınstanceandresourcegroupparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a3c6-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3c6-106">Stopbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6a3c6-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3c6-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a3c6-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a3c6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a3c6-108">DESCRIPTION</span></span>
<span data-ttu-id="6a3c6-109">Stop-AzSqlInstanceOperation cmdlet, SQL yönetilen örneğindeki işlem adına sahip olan işlemi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="6a3c6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a3c6-110">EXAMPLES</span></span>

### <span data-ttu-id="6a3c6-111">Örnek 1: belirli bir işlem edinme</span><span class="sxs-lookup"><span data-stu-id="6a3c6-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="6a3c6-112">Bu komut SQL yönetilen örneğindeki ' d0f5bef5-e2b1-4ef8-BB42-2e54073874f9 ' adlı işlemi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="6a3c6-113">Örnek 2: işlem kaynak kimliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="6a3c6-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="6a3c6-114">Bu komut, $managedInstanceOperation. ID kaynak kimliği ile işlemi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="6a3c6-115">Örnek 3: işlem nesnesini kullanma</span><span class="sxs-lookup"><span data-stu-id="6a3c6-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="6a3c6-116">Bu komut, nesne $managedInstanceOperation işlemi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="6a3c6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a3c6-117">PARAMETERS</span></span>

### <span data-ttu-id="6a3c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3c6-118">-DefaultProfile</span></span>
<span data-ttu-id="6a3c6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a3c6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6a3c6-120">-Force</span></span>
<span data-ttu-id="6a3c6-121">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="6a3c6-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6a3c6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a3c6-122">-InputObject</span></span>
<span data-ttu-id="6a3c6-123">İptal edilecek işlem</span><span class="sxs-lookup"><span data-stu-id="6a3c6-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3c6-124">-Managedınstancename</span><span class="sxs-lookup"><span data-stu-id="6a3c6-124">-ManagedInstanceName</span></span>
<span data-ttu-id="6a3c6-125">Örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3c6-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a3c6-126">-Name</span></span>
<span data-ttu-id="6a3c6-127">İşlemin adı.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a3c6-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3c6-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6a3c6-130">-ResourceId</span></span>
<span data-ttu-id="6a3c6-131">Durdurulacak işlem nesnesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6a3c6-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3c6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a3c6-132">-Confirm</span></span>
<span data-ttu-id="6a3c6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a3c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a3c6-134">-WhatIf</span></span>
<span data-ttu-id="6a3c6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a3c6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a3c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3c6-137">CommonParameters</span></span>
<span data-ttu-id="6a3c6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3c6-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6a3c6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3c6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a3c6-140">INPUTS</span></span>

### <span data-ttu-id="6a3c6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6a3c6-141">System.String</span></span>

### <span data-ttu-id="6a3c6-142">Microsoft. Azure. Commands. Sql. Managedınstanceoperation. model. Azurestabmanagedınstanceoperationmodel</span><span class="sxs-lookup"><span data-stu-id="6a3c6-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="6a3c6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a3c6-143">OUTPUTS</span></span>

### <span data-ttu-id="6a3c6-144">Microsoft. Azure. Commands. Sql. Managedınstanceoperation. model. Azurestabmanagedınstanceoperationmodel</span><span class="sxs-lookup"><span data-stu-id="6a3c6-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="6a3c6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a3c6-145">NOTES</span></span>

## <span data-ttu-id="6a3c6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a3c6-146">RELATED LINKS</span></span>
