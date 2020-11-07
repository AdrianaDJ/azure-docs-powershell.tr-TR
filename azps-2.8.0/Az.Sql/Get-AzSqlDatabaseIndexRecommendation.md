---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 009dcceb07b676e61eaa923e8b7ddecfbda3cfda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933668"
---
# <span data-ttu-id="46f86-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="46f86-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="46f86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f86-102">SYNOPSIS</span></span>
<span data-ttu-id="46f86-103">Sunucu veya veritabanı için önerilen dizin işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="46f86-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="46f86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46f86-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46f86-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46f86-105">DESCRIPTION</span></span>
<span data-ttu-id="46f86-106">**Get-Azsqldatabaseındextavsiyeleri** , BIR Azure SQL veritabanı sunucusu veya veritabanı için önerilen dizin işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="46f86-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="46f86-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46f86-107">EXAMPLES</span></span>

### <span data-ttu-id="46f86-108">Örnek 1: sunucudaki tüm veritabanları için Dizin önerilerini alma</span><span class="sxs-lookup"><span data-stu-id="46f86-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="46f86-109">Bu komut, sunucu server01 tüm veritabanları için Dizin önerilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="46f86-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="46f86-110">Örnek 2: belirli bir veritabanı için Dizin önerilerini alma</span><span class="sxs-lookup"><span data-stu-id="46f86-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="46f86-111">Bu komut, belirli veritabanı için Dizin önerilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="46f86-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="46f86-112">Örnek 3: ada göre tek bir dizin önerisi alma</span><span class="sxs-lookup"><span data-stu-id="46f86-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="46f86-113">Bu komut, ada göre tek dizin önerisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="46f86-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="46f86-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46f86-114">PARAMETERS</span></span>

### <span data-ttu-id="46f86-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46f86-115">-DatabaseName</span></span>
<span data-ttu-id="46f86-116">Bu cmdlet 'in Dizin önerilerini aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46f86-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f86-117">-DefaultProfile</span></span>
<span data-ttu-id="46f86-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="46f86-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46f86-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="46f86-119">-IndexRecommendationName</span></span>
<span data-ttu-id="46f86-120">Bu cmdlet 'in aldığı Dizin önerisi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46f86-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f86-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f86-121">-ResourceGroupName</span></span>
<span data-ttu-id="46f86-122">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46f86-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="46f86-123">Bu cmdlet, bu sunucuda barındırılan bir veritabanı için Dizin önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="46f86-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="46f86-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46f86-124">-ServerName</span></span>
<span data-ttu-id="46f86-125">Bu cmdlet 'in Dizin önerilerini aldığı veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46f86-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="46f86-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="46f86-126">-TableName</span></span>
<span data-ttu-id="46f86-127">Azure SQL tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46f86-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f86-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="46f86-128">-Confirm</span></span>
<span data-ttu-id="46f86-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46f86-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f86-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f86-130">-WhatIf</span></span>
<span data-ttu-id="46f86-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46f86-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f86-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46f86-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f86-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f86-133">CommonParameters</span></span>
<span data-ttu-id="46f86-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46f86-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f86-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46f86-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f86-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46f86-136">INPUTS</span></span>

### <span data-ttu-id="46f86-137">System. String</span><span class="sxs-lookup"><span data-stu-id="46f86-137">System.String</span></span>

## <span data-ttu-id="46f86-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46f86-138">OUTPUTS</span></span>

### <span data-ttu-id="46f86-139">Microsoft. Azure. Commands. Sql. model. ındexönerisi</span><span class="sxs-lookup"><span data-stu-id="46f86-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="46f86-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46f86-140">NOTES</span></span>

## <span data-ttu-id="46f86-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46f86-141">RELATED LINKS</span></span>

[<span data-ttu-id="46f86-142">Start-Azsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="46f86-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="46f86-143">Stop-Azsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="46f86-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
