---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098425"
---
# <span data-ttu-id="68b79-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="68b79-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="68b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b79-102">SYNOPSIS</span></span>
<span data-ttu-id="68b79-103">Azure SQL yönetilen veritabanı örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68b79-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="68b79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68b79-104">SYNTAX</span></span>

### <span data-ttu-id="68b79-105">Removeınstancefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68b79-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b79-106">Removeınstancefrolauressqlmanagedınstancemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="68b79-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b79-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="68b79-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b79-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="68b79-108">DESCRIPTION</span></span>
<span data-ttu-id="68b79-109">**Remove-Azsqlınstance** cmdlet 'ı, Azure SQL veritabanı yönetilen örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68b79-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="68b79-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68b79-110">EXAMPLES</span></span>

### <span data-ttu-id="68b79-111">Örnek 1: örneği kaldır</span><span class="sxs-lookup"><span data-stu-id="68b79-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="68b79-112">Bu komut, managedInstance1 adındaki örneği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68b79-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="68b79-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68b79-113">PARAMETERS</span></span>

### <span data-ttu-id="68b79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b79-114">-DefaultProfile</span></span>
<span data-ttu-id="68b79-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68b79-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b79-116">-Force</span><span class="sxs-lookup"><span data-stu-id="68b79-116">-Force</span></span>
<span data-ttu-id="68b79-117">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="68b79-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="68b79-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68b79-118">-InputObject</span></span>
<span data-ttu-id="68b79-119">Kaldırılacak Azurestabmanagedınstancemodel nesnesi</span><span class="sxs-lookup"><span data-stu-id="68b79-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68b79-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="68b79-120">-Name</span></span>
<span data-ttu-id="68b79-121">SQL örneği adı.</span><span class="sxs-lookup"><span data-stu-id="68b79-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b79-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b79-122">-ResourceGroupName</span></span>
<span data-ttu-id="68b79-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="68b79-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b79-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="68b79-124">-ResourceId</span></span>
<span data-ttu-id="68b79-125">Kaldırılacak örnek nesnenin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="68b79-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68b79-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="68b79-126">-Confirm</span></span>
<span data-ttu-id="68b79-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68b79-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b79-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b79-128">-WhatIf</span></span>
<span data-ttu-id="68b79-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68b79-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b79-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68b79-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b79-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b79-131">CommonParameters</span></span>
<span data-ttu-id="68b79-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68b79-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b79-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68b79-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b79-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68b79-134">INPUTS</span></span>

### <span data-ttu-id="68b79-135">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="68b79-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="68b79-136">System. String</span><span class="sxs-lookup"><span data-stu-id="68b79-136">System.String</span></span>

## <span data-ttu-id="68b79-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68b79-137">OUTPUTS</span></span>

### <span data-ttu-id="68b79-138">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="68b79-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="68b79-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68b79-139">NOTES</span></span>

## <span data-ttu-id="68b79-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68b79-140">RELATED LINKS</span></span>
