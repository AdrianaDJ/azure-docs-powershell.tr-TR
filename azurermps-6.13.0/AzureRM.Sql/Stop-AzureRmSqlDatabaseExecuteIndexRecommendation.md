---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 2922edf4f7b7cfd0d814a5559bb1e6e7bb9ef3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589285"
---
# <span data-ttu-id="e7efa-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="e7efa-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="e7efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7efa-102">SYNOPSIS</span></span>
<span data-ttu-id="e7efa-103">Önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e7efa-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7efa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7efa-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7efa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7efa-105">DESCRIPTION</span></span>
<span data-ttu-id="e7efa-106">**Stop-Azurermsqldatabaseexecuteındextavsiyi** , önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e7efa-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="e7efa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7efa-107">EXAMPLES</span></span>

### <span data-ttu-id="e7efa-108">Örnek 1: Dizin önerisini durdurma</span><span class="sxs-lookup"><span data-stu-id="e7efa-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="e7efa-109">Bu komut dizin önerisi çalıştırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="e7efa-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="e7efa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7efa-110">PARAMETERS</span></span>

### <span data-ttu-id="e7efa-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7efa-111">-DatabaseName</span></span>
<span data-ttu-id="e7efa-112">Bu cmdlet 'in iş akışını durdurduğu veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7efa-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="e7efa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7efa-113">-DefaultProfile</span></span>
<span data-ttu-id="e7efa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e7efa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7efa-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="e7efa-115">-IndexRecommendationName</span></span>
<span data-ttu-id="e7efa-116">Bu cmdlet 'in durduğu Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7efa-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e7efa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7efa-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7efa-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7efa-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e7efa-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7efa-119">-ServerName</span></span>
<span data-ttu-id="e7efa-120">Bu cmdlet 'in bir iş akışını durdurduğu veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7efa-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="e7efa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7efa-121">CommonParameters</span></span>
<span data-ttu-id="e7efa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7efa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7efa-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7efa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7efa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7efa-124">INPUTS</span></span>

### <span data-ttu-id="e7efa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e7efa-125">System.String</span></span>

## <span data-ttu-id="e7efa-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7efa-126">OUTPUTS</span></span>

### <span data-ttu-id="e7efa-127">Microsoft. Azure. Commands. Sql. model. ındexönerisi</span><span class="sxs-lookup"><span data-stu-id="e7efa-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="e7efa-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7efa-128">NOTES</span></span>

## <span data-ttu-id="e7efa-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7efa-129">RELATED LINKS</span></span>

[<span data-ttu-id="e7efa-130">Get-Azurermsqldatabaseındexönerileri</span><span class="sxs-lookup"><span data-stu-id="e7efa-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="e7efa-131">Start-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="e7efa-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="e7efa-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="e7efa-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


