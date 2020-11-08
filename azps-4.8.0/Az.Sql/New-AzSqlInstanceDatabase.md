---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108644"
---
# <span data-ttu-id="2b8d2-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2b8d2-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="2b8d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8d2-103">Azure SQL yönetilen örnek veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="2b8d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b8d2-104">SYNTAX</span></span>

### <span data-ttu-id="2b8d2-105">CreateNewInstanceDatabaseFromInputParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b8d2-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b8d2-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="2b8d2-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b8d2-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="2b8d2-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b8d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b8d2-108">DESCRIPTION</span></span>
<span data-ttu-id="2b8d2-109">**New-Azsqlınstancedatabase** cmdlet 'ı Azure SQL yönetilen örnek veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="2b8d2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b8d2-110">EXAMPLES</span></span>

### <span data-ttu-id="2b8d2-111">Örnek 1: belirtilen örnekte veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b8d2-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="2b8d2-112">Bu komut, managedInstance1 örneğinde Database01 adlı bir örnek veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="2b8d2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b8d2-113">PARAMETERS</span></span>

### <span data-ttu-id="2b8d2-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="2b8d2-114">-AsJob</span></span>
<span data-ttu-id="2b8d2-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2b8d2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b8d2-116">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="2b8d2-116">-Collation</span></span>
<span data-ttu-id="2b8d2-117">Kullanılacak Azure SQL örneği veritabanı harmanlaması harmanlaması.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="2b8d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8d2-118">-DefaultProfile</span></span>
<span data-ttu-id="2b8d2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b8d2-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2b8d2-120">-InstanceName</span></span>
<span data-ttu-id="2b8d2-121">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d2-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="2b8d2-122">-InstanceObject</span></span>
<span data-ttu-id="2b8d2-123">Örnek nesnesi</span><span class="sxs-lookup"><span data-stu-id="2b8d2-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d2-124">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="2b8d2-124">-InstanceResourceId</span></span>
<span data-ttu-id="2b8d2-125">Örnek kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2b8d2-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d2-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b8d2-126">-Name</span></span>
<span data-ttu-id="2b8d2-127">Oluşturulacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b8d2-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b8d2-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d2-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2b8d2-130">-Tag</span></span>
<span data-ttu-id="2b8d2-131">Azure SQL örneği veritabanıyla ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="2b8d2-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d2-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b8d2-132">-Confirm</span></span>
<span data-ttu-id="2b8d2-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b8d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b8d2-134">-WhatIf</span></span>
<span data-ttu-id="2b8d2-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b8d2-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b8d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8d2-137">CommonParameters</span></span>
<span data-ttu-id="2b8d2-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8d2-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2b8d2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8d2-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b8d2-140">INPUTS</span></span>

### <span data-ttu-id="2b8d2-141">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="2b8d2-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="2b8d2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2b8d2-142">System.String</span></span>

## <span data-ttu-id="2b8d2-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b8d2-143">OUTPUTS</span></span>

### <span data-ttu-id="2b8d2-144">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="2b8d2-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="2b8d2-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b8d2-145">NOTES</span></span>

## <span data-ttu-id="2b8d2-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b8d2-146">RELATED LINKS</span></span>
