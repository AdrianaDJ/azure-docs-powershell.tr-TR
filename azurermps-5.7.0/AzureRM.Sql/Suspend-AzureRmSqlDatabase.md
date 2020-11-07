---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/suspend-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: b4238ff85a35bcf6a48016a005af8a1f889332cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763943"
---
# <span data-ttu-id="79fb9-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79fb9-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="79fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="79fb9-103">SQL veri ambarı veritabanını askıya alır.</span><span class="sxs-lookup"><span data-stu-id="79fb9-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79fb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79fb9-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79fb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79fb9-105">DESCRIPTION</span></span>
<span data-ttu-id="79fb9-106">**Askıya al-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veri ambarı veritabanını askıya alır.</span><span class="sxs-lookup"><span data-stu-id="79fb9-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="79fb9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79fb9-107">EXAMPLES</span></span>

### <span data-ttu-id="79fb9-108">Örnek 1: Azure SQL veri ambarı veritabanını askıya alır</span><span class="sxs-lookup"><span data-stu-id="79fb9-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="79fb9-109">Bu komut, etkin bir Azure SQL veri ambarı veritabanını askıya alır.</span><span class="sxs-lookup"><span data-stu-id="79fb9-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="79fb9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79fb9-110">PARAMETERS</span></span>

### <span data-ttu-id="79fb9-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="79fb9-111">-AsJob</span></span>
<span data-ttu-id="79fb9-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="79fb9-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="79fb9-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79fb9-113">-DatabaseName</span></span>
<span data-ttu-id="79fb9-114">Bu cmdlet 'in askıya aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79fb9-114">Specifies the name of the database that this cmdlet suspends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fb9-115">-DefaultProfile</span></span>
<span data-ttu-id="79fb9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="79fb9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79fb9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79fb9-117">-ResourceGroupName</span></span>
<span data-ttu-id="79fb9-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79fb9-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fb9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79fb9-119">-ServerName</span></span>
<span data-ttu-id="79fb9-120">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79fb9-120">Specifies the name of the server which hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fb9-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="79fb9-121">-Confirm</span></span>
<span data-ttu-id="79fb9-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79fb9-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fb9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fb9-123">-WhatIf</span></span>
<span data-ttu-id="79fb9-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79fb9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79fb9-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79fb9-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fb9-126">CommonParameters</span></span>
<span data-ttu-id="79fb9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79fb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fb9-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fb9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fb9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79fb9-129">INPUTS</span></span>

### <span data-ttu-id="79fb9-130">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="79fb9-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="79fb9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79fb9-131">OUTPUTS</span></span>

### <span data-ttu-id="79fb9-132">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="79fb9-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="79fb9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79fb9-133">NOTES</span></span>
* <span data-ttu-id="79fb9-134">**Suspend-AzureRmSqlDatabase** cmdlet 'ı yalnızca Azure SQL veri ambarı veritabanlarında çalışır.</span><span class="sxs-lookup"><span data-stu-id="79fb9-134">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="79fb9-135">Bu işlem, Azure SQL veritabanı temel, Standard ve Premium sürümlerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="79fb9-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="79fb9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79fb9-136">RELATED LINKS</span></span>

[<span data-ttu-id="79fb9-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79fb9-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="79fb9-138">Yeni-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79fb9-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="79fb9-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79fb9-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="79fb9-140">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79fb9-140">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="79fb9-141">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79fb9-141">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="79fb9-142">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="79fb9-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


