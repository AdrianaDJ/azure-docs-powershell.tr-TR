---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: b3b09e9027a578809fe68a90630331ad6ee35943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594549"
---
# <span data-ttu-id="1342a-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="1342a-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="1342a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1342a-102">SYNOPSIS</span></span>
<span data-ttu-id="1342a-103">Sunucu veya veritabanı için önerilen dizin işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1342a-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1342a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1342a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1342a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1342a-105">DESCRIPTION</span></span>
<span data-ttu-id="1342a-106">**Get-Azurermsqldatabaseındextavsiyeleri** , BIR Azure SQL veritabanı sunucusu veya veritabanı için önerilen dizin işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1342a-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="1342a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1342a-107">EXAMPLES</span></span>

### <span data-ttu-id="1342a-108">Örnek 1: sunucudaki tüm veritabanları için Dizin önerilerini alma</span><span class="sxs-lookup"><span data-stu-id="1342a-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="1342a-109">Bu komut, sunucu server01 tüm veritabanları için Dizin önerilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1342a-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="1342a-110">Örnek 2: belirli bir veritabanı için Dizin önerilerini alma</span><span class="sxs-lookup"><span data-stu-id="1342a-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1342a-111">Bu komut, belirli veritabanı için Dizin önerilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1342a-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="1342a-112">Örnek 3: ada göre tek bir dizin önerisi alma</span><span class="sxs-lookup"><span data-stu-id="1342a-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="1342a-113">Bu komut, ada göre tek dizin önerisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="1342a-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="1342a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1342a-114">PARAMETERS</span></span>

### <span data-ttu-id="1342a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1342a-115">-DatabaseName</span></span>
<span data-ttu-id="1342a-116">Bu cmdlet 'in Dizin önerilerini aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1342a-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="1342a-117">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="1342a-117">-IndexRecommendationName</span></span>
<span data-ttu-id="1342a-118">Bu cmdlet 'in aldığı Dizin önerisi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1342a-118">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1342a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1342a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1342a-120">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1342a-120">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="1342a-121">Bu cmdlet, bu sunucuda barındırılan bir veritabanı için Dizin önerilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1342a-121">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="1342a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1342a-122">-ServerName</span></span>
<span data-ttu-id="1342a-123">Bu cmdlet 'in Dizin önerilerini aldığı veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1342a-123">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="1342a-124">-TableName</span><span class="sxs-lookup"><span data-stu-id="1342a-124">-TableName</span></span>
<span data-ttu-id="1342a-125">Azure SQL tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1342a-125">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="1342a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="1342a-126">-Confirm</span></span>
<span data-ttu-id="1342a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1342a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1342a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1342a-128">-WhatIf</span></span>
<span data-ttu-id="1342a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1342a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1342a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1342a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1342a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1342a-131">-DefaultProfile</span></span>
<span data-ttu-id="1342a-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1342a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1342a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1342a-133">CommonParameters</span></span>
<span data-ttu-id="1342a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1342a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1342a-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1342a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1342a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1342a-136">INPUTS</span></span>

## <span data-ttu-id="1342a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1342a-137">OUTPUTS</span></span>

## <span data-ttu-id="1342a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1342a-138">NOTES</span></span>

## <span data-ttu-id="1342a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1342a-139">RELATED LINKS</span></span>

[<span data-ttu-id="1342a-140">Start-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="1342a-140">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="1342a-141">Stop-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="1342a-141">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)