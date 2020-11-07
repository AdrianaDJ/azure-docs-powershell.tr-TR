---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763207"
---
# <span data-ttu-id="fef99-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="fef99-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="fef99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef99-102">SYNOPSIS</span></span>
<span data-ttu-id="fef99-103">Önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="fef99-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fef99-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fef99-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fef99-105">DESCRIPTION</span></span>
<span data-ttu-id="fef99-106">**Stop-Azurermsqldatabaseexecuteındextavsiyi** , önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="fef99-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="fef99-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fef99-107">EXAMPLES</span></span>

### <span data-ttu-id="fef99-108">Örnek 1: Dizin önerisini durdurma</span><span class="sxs-lookup"><span data-stu-id="fef99-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="fef99-109">Bu komut dizin önerisi çalıştırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="fef99-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="fef99-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fef99-110">PARAMETERS</span></span>

### <span data-ttu-id="fef99-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fef99-111">-DatabaseName</span></span>
<span data-ttu-id="fef99-112">Bu cmdlet 'in iş akışını durdurduğu veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef99-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="fef99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef99-113">-DefaultProfile</span></span>
<span data-ttu-id="fef99-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fef99-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fef99-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="fef99-115">-IndexRecommendationName</span></span>
<span data-ttu-id="fef99-116">Bu cmdlet 'in durduğu Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef99-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="fef99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef99-117">-ResourceGroupName</span></span>
<span data-ttu-id="fef99-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef99-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fef99-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fef99-119">-ServerName</span></span>
<span data-ttu-id="fef99-120">Bu cmdlet 'in bir iş akışını durdurduğu veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef99-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="fef99-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef99-121">CommonParameters</span></span>
<span data-ttu-id="fef99-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fef99-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef99-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef99-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef99-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fef99-124">INPUTS</span></span>

### <span data-ttu-id="fef99-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fef99-125">None</span></span>
<span data-ttu-id="fef99-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fef99-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fef99-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fef99-127">OUTPUTS</span></span>

## <span data-ttu-id="fef99-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fef99-128">NOTES</span></span>

## <span data-ttu-id="fef99-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fef99-129">RELATED LINKS</span></span>

[<span data-ttu-id="fef99-130">Get-Azurermsqldatabaseındexönerileri</span><span class="sxs-lookup"><span data-stu-id="fef99-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="fef99-131">Start-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="fef99-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="fef99-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="fef99-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


