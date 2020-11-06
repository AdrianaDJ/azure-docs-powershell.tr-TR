---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 2ef6ff642d22429ae22186ce01a4a17dad125b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590827"
---
# <span data-ttu-id="6a5ab-101">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6a5ab-101">New-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="6a5ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5ab-103">Azure SQL yönetilen örnek veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-103">Creates an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a5ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a5ab-104">SYNTAX</span></span>

### <span data-ttu-id="6a5ab-105">CreateNewInstanceDatabaseFromInputParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a5ab-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a5ab-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6a5ab-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a5ab-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="6a5ab-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a5ab-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a5ab-108">DESCRIPTION</span></span>
<span data-ttu-id="6a5ab-109">**Yeni-Azurermsqlınstancedatabase** cmdlet 'ı Azure SQL yönetilen örnek veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-109">The **New-AzureRmSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="6a5ab-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a5ab-110">EXAMPLES</span></span>

### <span data-ttu-id="6a5ab-111">Örnek 1: belirtilen örnekte veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a5ab-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="6a5ab-112">Bu komut, managedInstance1 örneğinde Database01 adlı bir örnek veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="6a5ab-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a5ab-113">PARAMETERS</span></span>

### <span data-ttu-id="6a5ab-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="6a5ab-114">-AsJob</span></span>
<span data-ttu-id="6a5ab-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6a5ab-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a5ab-116">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="6a5ab-116">-Collation</span></span>
<span data-ttu-id="6a5ab-117">Kullanılacak Azure SQL örneği veritabanı harmanlaması harmanlaması.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5ab-118">-DefaultProfile</span></span>
<span data-ttu-id="6a5ab-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5ab-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6a5ab-120">-InstanceName</span></span>
<span data-ttu-id="6a5ab-121">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ab-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="6a5ab-122">-InstanceObject</span></span>
<span data-ttu-id="6a5ab-123">Örnek nesnesi</span><span class="sxs-lookup"><span data-stu-id="6a5ab-123">The instance object</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ab-124">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="6a5ab-124">-InstanceResourceId</span></span>
<span data-ttu-id="6a5ab-125">Örnek kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6a5ab-125">The instance resource id</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ab-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a5ab-126">-Name</span></span>
<span data-ttu-id="6a5ab-127">Oluşturulacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a5ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a5ab-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ab-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6a5ab-130">-Tag</span></span>
<span data-ttu-id="6a5ab-131">Azure SQL örneği veritabanıyla ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="6a5ab-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5ab-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a5ab-132">-Confirm</span></span>
<span data-ttu-id="6a5ab-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a5ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a5ab-134">-WhatIf</span></span>
<span data-ttu-id="6a5ab-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a5ab-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a5ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5ab-137">CommonParameters</span></span>
<span data-ttu-id="6a5ab-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a5ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5ab-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a5ab-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5ab-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a5ab-140">INPUTS</span></span>

### <span data-ttu-id="6a5ab-141">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="6a5ab-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="6a5ab-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6a5ab-142">System.String</span></span>

## <span data-ttu-id="6a5ab-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a5ab-143">OUTPUTS</span></span>

### <span data-ttu-id="6a5ab-144">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="6a5ab-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6a5ab-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a5ab-145">NOTES</span></span>

## <span data-ttu-id="6a5ab-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a5ab-146">RELATED LINKS</span></span>
