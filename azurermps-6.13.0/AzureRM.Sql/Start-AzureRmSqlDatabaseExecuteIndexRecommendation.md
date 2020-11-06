---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c61f1bd988410b696eddd12162958333022dd892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589295"
---
# <span data-ttu-id="d0cc0-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d0cc0-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="d0cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cc0-103">Önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0cc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0cc0-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0cc0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="d0cc0-106">**Start-Azurermsqldatabaseexecuteındexöneri** cmdlet 'i, BIR Azure SQL veritabanı için önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="d0cc0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="d0cc0-108">Örnek 1: Dizin önerisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d0cc0-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="d0cc0-109">Bu komut bir dizin önerisi çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="d0cc0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0cc0-110">PARAMETERS</span></span>

### <span data-ttu-id="d0cc0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0cc0-111">-DatabaseName</span></span>
<span data-ttu-id="d0cc0-112">Bu cmdlet 'in iş akışını başlattığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="d0cc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cc0-113">-DefaultProfile</span></span>
<span data-ttu-id="d0cc0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d0cc0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0cc0-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="d0cc0-115">-IndexRecommendationName</span></span>
<span data-ttu-id="d0cc0-116">Bu cmdlet 'in çalıştığı Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="d0cc0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0cc0-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0cc0-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d0cc0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0cc0-119">-ServerName</span></span>
<span data-ttu-id="d0cc0-120">Bu cmdlet 'in iş akışını başlattığı veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="d0cc0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cc0-121">CommonParameters</span></span>
<span data-ttu-id="d0cc0-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0cc0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cc0-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0cc0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cc0-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0cc0-124">INPUTS</span></span>

### <span data-ttu-id="d0cc0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d0cc0-125">System.String</span></span>

## <span data-ttu-id="d0cc0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0cc0-126">OUTPUTS</span></span>

### <span data-ttu-id="d0cc0-127">Microsoft. Azure. Commands. Sql. model. ındexönerisi</span><span class="sxs-lookup"><span data-stu-id="d0cc0-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="d0cc0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0cc0-128">NOTES</span></span>

## <span data-ttu-id="d0cc0-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0cc0-129">RELATED LINKS</span></span>

[<span data-ttu-id="d0cc0-130">Get-Azurermsqldatabaseındexönerileri</span><span class="sxs-lookup"><span data-stu-id="d0cc0-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="d0cc0-131">Stop-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="d0cc0-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="d0cc0-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="d0cc0-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


