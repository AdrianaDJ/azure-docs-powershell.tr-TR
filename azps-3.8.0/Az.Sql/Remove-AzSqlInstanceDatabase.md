---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098287"
---
# <span data-ttu-id="d3645-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d3645-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="d3645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3645-102">SYNOPSIS</span></span>
<span data-ttu-id="d3645-103">Azure SQL yönetilen örneği veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3645-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d3645-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3645-104">SYNTAX</span></span>

### <span data-ttu-id="d3645-105">Removeınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3645-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3645-106">Removeınstancedatabasefrolaurestarmanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="d3645-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3645-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d3645-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3645-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3645-108">DESCRIPTION</span></span>
<span data-ttu-id="d3645-109">**Remove-Azsqlınstancedatabase** cmdlet 'ı BIR Azure SQL yönetilen örneği veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3645-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d3645-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3645-110">EXAMPLES</span></span>

### <span data-ttu-id="d3645-111">Örnek 1: örnekten veritabanı kaldırma</span><span class="sxs-lookup"><span data-stu-id="d3645-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d3645-112">Bu komut, managedInstance1 örneğindeki Database01 adlı veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3645-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="d3645-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3645-113">PARAMETERS</span></span>

### <span data-ttu-id="d3645-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3645-114">-DefaultProfile</span></span>
<span data-ttu-id="d3645-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3645-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3645-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d3645-116">-Force</span></span>
<span data-ttu-id="d3645-117">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="d3645-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d3645-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3645-118">-InputObject</span></span>
<span data-ttu-id="d3645-119">Kaldırılacak örnek veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d3645-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d3645-120">-InstanceName</span></span>
<span data-ttu-id="d3645-121">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="d3645-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3645-122">-Name</span></span>
<span data-ttu-id="d3645-123">Kaldırılacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d3645-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3645-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3645-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d3645-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3645-126">-ResourceId</span></span>
<span data-ttu-id="d3645-127">Kaldırılacak örnek veritabanı nesnesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d3645-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3645-128">-Confirm</span></span>
<span data-ttu-id="d3645-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3645-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3645-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3645-130">-WhatIf</span></span>
<span data-ttu-id="d3645-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3645-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3645-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3645-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3645-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3645-133">CommonParameters</span></span>
<span data-ttu-id="d3645-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3645-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3645-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d3645-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3645-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3645-136">INPUTS</span></span>

### <span data-ttu-id="d3645-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="d3645-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="d3645-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d3645-138">System.String</span></span>

## <span data-ttu-id="d3645-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3645-139">OUTPUTS</span></span>

### <span data-ttu-id="d3645-140">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="d3645-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d3645-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3645-141">NOTES</span></span>

## <span data-ttu-id="d3645-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3645-142">RELATED LINKS</span></span>
