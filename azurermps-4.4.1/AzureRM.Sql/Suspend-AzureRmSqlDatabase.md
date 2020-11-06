---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593777"
---
# <span data-ttu-id="ee548-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee548-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ee548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee548-102">SYNOPSIS</span></span>
<span data-ttu-id="ee548-103">SQL veri ambarı veritabanını askıya alır.</span><span class="sxs-lookup"><span data-stu-id="ee548-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee548-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee548-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee548-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee548-105">DESCRIPTION</span></span>
<span data-ttu-id="ee548-106">**Askıya al-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veri ambarı veritabanını askıya alır.</span><span class="sxs-lookup"><span data-stu-id="ee548-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="ee548-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee548-107">EXAMPLES</span></span>

### <span data-ttu-id="ee548-108">Örnek 1: Azure SQL veri ambarı veritabanını askıya alır</span><span class="sxs-lookup"><span data-stu-id="ee548-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ee548-109">Bu komut, etkin bir Azure SQL veri ambarı veritabanını askıya alır.</span><span class="sxs-lookup"><span data-stu-id="ee548-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="ee548-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee548-110">PARAMETERS</span></span>

### <span data-ttu-id="ee548-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee548-111">-DatabaseName</span></span>
<span data-ttu-id="ee548-112">Bu cmdlet 'in askıya aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee548-112">Specifies the name of the database that this cmdlet suspends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee548-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee548-113">-ResourceGroupName</span></span>
<span data-ttu-id="ee548-114">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee548-114">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee548-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee548-115">-ServerName</span></span>
<span data-ttu-id="ee548-116">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee548-116">Specifies the name of the server which hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee548-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee548-117">-Confirm</span></span>
<span data-ttu-id="ee548-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee548-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee548-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee548-119">-WhatIf</span></span>
<span data-ttu-id="ee548-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee548-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee548-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee548-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee548-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee548-122">-DefaultProfile</span></span>
<span data-ttu-id="ee548-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee548-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee548-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee548-124">CommonParameters</span></span>
<span data-ttu-id="ee548-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee548-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee548-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee548-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee548-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee548-127">INPUTS</span></span>

### <span data-ttu-id="ee548-128">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="ee548-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ee548-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee548-129">OUTPUTS</span></span>

### <span data-ttu-id="ee548-130">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="ee548-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ee548-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee548-131">NOTES</span></span>
* <span data-ttu-id="ee548-132">**Suspend-AzureRmSqlDatabase** cmdlet 'ı yalnızca Azure SQL veri ambarı veritabanlarında çalışır.</span><span class="sxs-lookup"><span data-stu-id="ee548-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="ee548-133">Bu işlem, Azure SQL veritabanı temel, Standard ve Premium sürümlerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="ee548-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="ee548-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee548-134">RELATED LINKS</span></span>

[<span data-ttu-id="ee548-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee548-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee548-136">Yeni-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee548-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee548-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee548-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee548-138">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee548-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee548-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ee548-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="ee548-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ee548-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


