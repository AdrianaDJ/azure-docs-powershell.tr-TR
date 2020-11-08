---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937970"
---
# <span data-ttu-id="ba835-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ba835-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ba835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba835-102">SYNOPSIS</span></span>
<span data-ttu-id="ba835-103">Önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="ba835-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ba835-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba835-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba835-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba835-105">DESCRIPTION</span></span>
<span data-ttu-id="ba835-106">**Stop-Azsqldatabaseexecuteındextavsiyi** , önerilen dizin işlemini çalıştıran iş akışını durdurur.</span><span class="sxs-lookup"><span data-stu-id="ba835-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ba835-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba835-107">EXAMPLES</span></span>

### <span data-ttu-id="ba835-108">Örnek 1: Dizin önerisini durdurma</span><span class="sxs-lookup"><span data-stu-id="ba835-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ba835-109">Bu komut dizin önerisi çalıştırmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="ba835-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="ba835-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba835-110">PARAMETERS</span></span>

### <span data-ttu-id="ba835-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba835-111">-DatabaseName</span></span>
<span data-ttu-id="ba835-112">Bu cmdlet 'in iş akışını durdurduğu veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba835-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="ba835-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba835-113">-DefaultProfile</span></span>
<span data-ttu-id="ba835-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba835-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba835-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ba835-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ba835-116">Bu cmdlet 'in durduğu Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba835-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="ba835-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba835-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba835-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba835-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ba835-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba835-119">-ServerName</span></span>
<span data-ttu-id="ba835-120">Bu cmdlet 'in bir iş akışını durdurduğu veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba835-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="ba835-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba835-121">CommonParameters</span></span>
<span data-ttu-id="ba835-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba835-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba835-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba835-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba835-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba835-124">INPUTS</span></span>

### <span data-ttu-id="ba835-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ba835-125">System.String</span></span>

## <span data-ttu-id="ba835-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba835-126">OUTPUTS</span></span>

### <span data-ttu-id="ba835-127">Microsoft. Azure. Commands. Sql. model. ındexönerisi</span><span class="sxs-lookup"><span data-stu-id="ba835-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ba835-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba835-128">NOTES</span></span>

## <span data-ttu-id="ba835-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba835-129">RELATED LINKS</span></span>

[<span data-ttu-id="ba835-130">Get-Azsqldatabaseındexönerisi</span><span class="sxs-lookup"><span data-stu-id="ba835-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="ba835-131">Start-Azsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="ba835-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ba835-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ba835-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

