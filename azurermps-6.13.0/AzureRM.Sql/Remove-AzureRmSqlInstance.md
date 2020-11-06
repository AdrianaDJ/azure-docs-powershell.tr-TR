---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593180"
---
# <span data-ttu-id="f2ca8-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f2ca8-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="f2ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ca8-103">Azure SQL yönetilen veritabanı örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2ca8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2ca8-104">SYNTAX</span></span>

### <span data-ttu-id="f2ca8-105">Removeınstancefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2ca8-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2ca8-106">Removeınstancefrolauressqlmanagedınstancemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="f2ca8-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2ca8-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f2ca8-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2ca8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2ca8-108">DESCRIPTION</span></span>
<span data-ttu-id="f2ca8-109">**Remove-Azurermsqlınstance** cmdlet 'ı, Azure SQL veritabanı yönetilen örneğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="f2ca8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2ca8-110">EXAMPLES</span></span>

### <span data-ttu-id="f2ca8-111">Örnek 1: örneği kaldır</span><span class="sxs-lookup"><span data-stu-id="f2ca8-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f2ca8-112">Bu komut, managedInstance1 adındaki örneği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="f2ca8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2ca8-113">PARAMETERS</span></span>

### <span data-ttu-id="f2ca8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ca8-114">-DefaultProfile</span></span>
<span data-ttu-id="f2ca8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2ca8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f2ca8-116">-Force</span></span>
<span data-ttu-id="f2ca8-117">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="f2ca8-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f2ca8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2ca8-118">-InputObject</span></span>
<span data-ttu-id="f2ca8-119">Kaldırılacak Azurestabmanagedınstancemodel nesnesi</span><span class="sxs-lookup"><span data-stu-id="f2ca8-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ca8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2ca8-120">-Name</span></span>
<span data-ttu-id="f2ca8-121">SQL örneği adı.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ca8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ca8-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2ca8-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ca8-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f2ca8-124">-ResourceId</span></span>
<span data-ttu-id="f2ca8-125">Kaldırılacak örnek nesnenin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f2ca8-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ca8-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2ca8-126">-Confirm</span></span>
<span data-ttu-id="f2ca8-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2ca8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2ca8-128">-WhatIf</span></span>
<span data-ttu-id="f2ca8-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2ca8-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2ca8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ca8-131">CommonParameters</span></span>
<span data-ttu-id="f2ca8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ca8-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ca8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ca8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2ca8-134">INPUTS</span></span>

### <span data-ttu-id="f2ca8-135">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="f2ca8-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="f2ca8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f2ca8-136">System.String</span></span>

## <span data-ttu-id="f2ca8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2ca8-137">OUTPUTS</span></span>

### <span data-ttu-id="f2ca8-138">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="f2ca8-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="f2ca8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2ca8-139">NOTES</span></span>

## <span data-ttu-id="f2ca8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2ca8-140">RELATED LINKS</span></span>
