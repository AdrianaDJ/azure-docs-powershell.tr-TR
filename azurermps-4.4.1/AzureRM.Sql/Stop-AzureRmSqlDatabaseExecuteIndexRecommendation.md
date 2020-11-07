---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 4fef918efd69d1ef5506efb70f1db94903845a8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764208"
---
# <span data-ttu-id="e173f-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="e173f-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="e173f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e173f-102">SYNOPSIS</span></span>
<span data-ttu-id="e173f-103">Önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e173f-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e173f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e173f-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e173f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e173f-105">DESCRIPTION</span></span>
<span data-ttu-id="e173f-106">**Stop-Azurermsqldatabaseexecuteındextavsiyi** , önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="e173f-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="e173f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e173f-107">EXAMPLES</span></span>

### <span data-ttu-id="e173f-108">Örnek 1: Dizin önerisini durdurma</span><span class="sxs-lookup"><span data-stu-id="e173f-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="e173f-109">Bu komut dizin önerisi çalıştırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="e173f-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="e173f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e173f-110">PARAMETERS</span></span>

### <span data-ttu-id="e173f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e173f-111">-DatabaseName</span></span>
<span data-ttu-id="e173f-112">Bu cmdlet 'in iş akışını durdurduğu veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e173f-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="e173f-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="e173f-113">-IndexRecommendationName</span></span>
<span data-ttu-id="e173f-114">Bu cmdlet 'in durduğu Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e173f-114">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e173f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e173f-115">-ResourceGroupName</span></span>
<span data-ttu-id="e173f-116">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e173f-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e173f-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e173f-117">-ServerName</span></span>
<span data-ttu-id="e173f-118">Bu cmdlet 'in bir iş akışını durdurduğu veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e173f-118">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="e173f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e173f-119">-DefaultProfile</span></span>
<span data-ttu-id="e173f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e173f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e173f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e173f-121">CommonParameters</span></span>
<span data-ttu-id="e173f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e173f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e173f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e173f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e173f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e173f-124">INPUTS</span></span>

## <span data-ttu-id="e173f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e173f-125">OUTPUTS</span></span>

## <span data-ttu-id="e173f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e173f-126">NOTES</span></span>

## <span data-ttu-id="e173f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e173f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e173f-128">Get-Azurermsqldatabaseındexönerileri</span><span class="sxs-lookup"><span data-stu-id="e173f-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="e173f-129">Start-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="e173f-129">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="e173f-130">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="e173f-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


