---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: f391dbb5d3e70e486a91c1dbb9e6517936bd2b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593179"
---
# <span data-ttu-id="58714-101">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="58714-101">Remove-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="58714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58714-102">SYNOPSIS</span></span>
<span data-ttu-id="58714-103">Azure SQL yönetilen örneği veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="58714-103">Removes an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58714-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58714-104">SYNTAX</span></span>

### <span data-ttu-id="58714-105">Removeınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58714-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58714-106">Removeınstancedatabasefrolaurestarmanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="58714-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58714-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="58714-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58714-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="58714-108">DESCRIPTION</span></span>
<span data-ttu-id="58714-109">**Remove-Azurermsqlınstancedatabase** cmdlet 'ı BIR Azure SQL yönetilen örneği veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="58714-109">The **Remove-AzureRmSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="58714-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58714-110">EXAMPLES</span></span>

### <span data-ttu-id="58714-111">Örnek 1: örnekten veritabanı kaldırma</span><span class="sxs-lookup"><span data-stu-id="58714-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58714-112">Bu komut, managedInstance1 örneğindeki Database01 adlı veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="58714-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="58714-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58714-113">PARAMETERS</span></span>

### <span data-ttu-id="58714-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58714-114">-DefaultProfile</span></span>
<span data-ttu-id="58714-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58714-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58714-116">-Force</span><span class="sxs-lookup"><span data-stu-id="58714-116">-Force</span></span>
<span data-ttu-id="58714-117">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="58714-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="58714-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58714-118">-InputObject</span></span>
<span data-ttu-id="58714-119">Kaldırılacak örnek veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="58714-119">The Instance Database object to remove</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58714-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="58714-120">-InstanceName</span></span>
<span data-ttu-id="58714-121">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="58714-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58714-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="58714-122">-Name</span></span>
<span data-ttu-id="58714-123">Kaldırılacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="58714-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58714-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58714-124">-ResourceGroupName</span></span>
<span data-ttu-id="58714-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="58714-125">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58714-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="58714-126">-ResourceId</span></span>
<span data-ttu-id="58714-127">Kaldırılacak örnek veritabanı nesnesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="58714-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58714-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="58714-128">-Confirm</span></span>
<span data-ttu-id="58714-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58714-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58714-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58714-130">-WhatIf</span></span>
<span data-ttu-id="58714-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58714-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58714-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58714-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58714-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58714-133">CommonParameters</span></span>
<span data-ttu-id="58714-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58714-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58714-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58714-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58714-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58714-136">INPUTS</span></span>

### <span data-ttu-id="58714-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="58714-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="58714-138">System. String</span><span class="sxs-lookup"><span data-stu-id="58714-138">System.String</span></span>

## <span data-ttu-id="58714-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58714-139">OUTPUTS</span></span>

### <span data-ttu-id="58714-140">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="58714-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="58714-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58714-141">NOTES</span></span>

## <span data-ttu-id="58714-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58714-142">RELATED LINKS</span></span>
