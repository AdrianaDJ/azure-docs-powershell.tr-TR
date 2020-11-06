---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 3da5093decdaea29d1a225db5c683d2f23f7115f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591552"
---
# <span data-ttu-id="ab590-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab590-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ab590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab590-102">SYNOPSIS</span></span>
<span data-ttu-id="ab590-103">Azure SQL veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ab590-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab590-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab590-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab590-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab590-105">DESCRIPTION</span></span>
<span data-ttu-id="ab590-106">**Remove-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ab590-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="ab590-107">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="ab590-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ab590-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab590-108">EXAMPLES</span></span>

### <span data-ttu-id="ab590-109">Örnek 1: Azure SQL Server 'dan veritabanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ab590-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ab590-110">Bu komut, Database01 adlı veritabanını sunucudan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ab590-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="ab590-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab590-111">PARAMETERS</span></span>

### <span data-ttu-id="ab590-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab590-112">-DatabaseName</span></span>
<span data-ttu-id="ab590-113">Bu cmdlet 'in kaldırdığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab590-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab590-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab590-114">-DefaultProfile</span></span>
<span data-ttu-id="ab590-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ab590-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab590-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ab590-116">-Force</span></span>
<span data-ttu-id="ab590-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ab590-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab590-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab590-118">-ResourceGroupName</span></span>
<span data-ttu-id="ab590-119">Veritabanının atandığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab590-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ab590-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ab590-120">-ServerName</span></span>
<span data-ttu-id="ab590-121">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab590-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ab590-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab590-122">-Confirm</span></span>
<span data-ttu-id="ab590-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab590-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab590-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab590-124">-WhatIf</span></span>
<span data-ttu-id="ab590-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab590-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab590-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab590-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab590-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab590-127">CommonParameters</span></span>
<span data-ttu-id="ab590-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab590-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab590-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab590-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab590-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab590-130">INPUTS</span></span>

### <span data-ttu-id="ab590-131">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="ab590-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ab590-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab590-132">OUTPUTS</span></span>

### <span data-ttu-id="ab590-133">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="ab590-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ab590-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab590-134">NOTES</span></span>

## <span data-ttu-id="ab590-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab590-135">RELATED LINKS</span></span>

[<span data-ttu-id="ab590-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab590-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ab590-137">Yeni-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab590-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="ab590-138">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab590-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ab590-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab590-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="ab590-140">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab590-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="ab590-141">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ab590-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


