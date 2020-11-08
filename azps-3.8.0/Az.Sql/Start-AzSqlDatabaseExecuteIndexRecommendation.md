---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937985"
---
# <span data-ttu-id="69ed4-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="69ed4-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="69ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="69ed4-103">Önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="69ed4-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="69ed4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69ed4-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69ed4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="69ed4-106">**Start-Azsqldatabaseexecuteındextavsiyeleri** , BIR Azure SQL veritabanı için önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="69ed4-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="69ed4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69ed4-107">EXAMPLES</span></span>

### <span data-ttu-id="69ed4-108">Örnek 1: Dizin önerisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="69ed4-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="69ed4-109">Bu komut bir dizin önerisi çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="69ed4-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="69ed4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69ed4-110">PARAMETERS</span></span>

### <span data-ttu-id="69ed4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69ed4-111">-DatabaseName</span></span>
<span data-ttu-id="69ed4-112">Bu cmdlet 'in iş akışını başlattığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69ed4-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="69ed4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ed4-113">-DefaultProfile</span></span>
<span data-ttu-id="69ed4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69ed4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69ed4-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="69ed4-115">-IndexRecommendationName</span></span>
<span data-ttu-id="69ed4-116">Bu cmdlet 'in çalıştığı Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69ed4-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="69ed4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ed4-117">-ResourceGroupName</span></span>
<span data-ttu-id="69ed4-118">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69ed4-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="69ed4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69ed4-119">-ServerName</span></span>
<span data-ttu-id="69ed4-120">Bu cmdlet 'in iş akışını başlattığı veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="69ed4-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="69ed4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ed4-121">CommonParameters</span></span>
<span data-ttu-id="69ed4-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69ed4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ed4-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69ed4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ed4-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69ed4-124">INPUTS</span></span>

### <span data-ttu-id="69ed4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="69ed4-125">System.String</span></span>

## <span data-ttu-id="69ed4-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69ed4-126">OUTPUTS</span></span>

### <span data-ttu-id="69ed4-127">Microsoft. Azure. Commands. Sql. model. ındexönerisi</span><span class="sxs-lookup"><span data-stu-id="69ed4-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="69ed4-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69ed4-128">NOTES</span></span>

## <span data-ttu-id="69ed4-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69ed4-129">RELATED LINKS</span></span>

[<span data-ttu-id="69ed4-130">Get-Azsqldatabaseındexönerisi</span><span class="sxs-lookup"><span data-stu-id="69ed4-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="69ed4-131">Stop-Azsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="69ed4-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="69ed4-132">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="69ed4-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

