---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ac5bf33bd87ff290784728fd0c4857d5278d3057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591544"
---
# <span data-ttu-id="951f4-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="951f4-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="951f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="951f4-102">SYNOPSIS</span></span>
<span data-ttu-id="951f4-103">Önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="951f4-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="951f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="951f4-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="951f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="951f4-105">DESCRIPTION</span></span>
<span data-ttu-id="951f4-106">**Start-Azurermsqldatabaseexecuteındexöneri** cmdlet 'i, BIR Azure SQL veritabanı için önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="951f4-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="951f4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="951f4-107">EXAMPLES</span></span>

### <span data-ttu-id="951f4-108">Örnek 1: Dizin önerisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="951f4-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="951f4-109">Bu komut bir dizin önerisi çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="951f4-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="951f4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="951f4-110">PARAMETERS</span></span>

### <span data-ttu-id="951f4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="951f4-111">-DatabaseName</span></span>
<span data-ttu-id="951f4-112">Bu cmdlet 'in iş akışını başlattığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="951f4-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="951f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951f4-113">-DefaultProfile</span></span>
<span data-ttu-id="951f4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="951f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="951f4-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="951f4-115">-IndexRecommendationName</span></span>
<span data-ttu-id="951f4-116">Bu cmdlet 'in çalıştığı Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="951f4-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="951f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="951f4-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="951f4-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="951f4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="951f4-119">-ServerName</span></span>
<span data-ttu-id="951f4-120">Bu cmdlet 'in iş akışını başlattığı veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="951f4-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="951f4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951f4-121">CommonParameters</span></span>
<span data-ttu-id="951f4-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="951f4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951f4-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="951f4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951f4-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="951f4-124">INPUTS</span></span>

### <span data-ttu-id="951f4-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="951f4-125">None</span></span>
<span data-ttu-id="951f4-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="951f4-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="951f4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="951f4-127">OUTPUTS</span></span>

## <span data-ttu-id="951f4-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="951f4-128">NOTES</span></span>

## <span data-ttu-id="951f4-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="951f4-129">RELATED LINKS</span></span>

[<span data-ttu-id="951f4-130">Get-Azurermsqldatabaseındexönerileri</span><span class="sxs-lookup"><span data-stu-id="951f4-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="951f4-131">Stop-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="951f4-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="951f4-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="951f4-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


