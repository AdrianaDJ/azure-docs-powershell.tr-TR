---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ae4564b1f583b8057438ee631de6b13d38e008ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764210"
---
# <span data-ttu-id="c9148-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c9148-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="c9148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9148-102">SYNOPSIS</span></span>
<span data-ttu-id="c9148-103">Önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="c9148-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9148-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9148-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9148-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9148-105">DESCRIPTION</span></span>
<span data-ttu-id="c9148-106">**Start-Azurermsqldatabaseexecuteındexöneri** cmdlet 'i, BIR Azure SQL veritabanı için önerilen dizin işlemini çalıştıran iş akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="c9148-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="c9148-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9148-107">EXAMPLES</span></span>

### <span data-ttu-id="c9148-108">Örnek 1: Dizin önerisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9148-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="c9148-109">Bu komut bir dizin önerisi çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="c9148-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="c9148-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9148-110">PARAMETERS</span></span>

### <span data-ttu-id="c9148-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9148-111">-DatabaseName</span></span>
<span data-ttu-id="c9148-112">Bu cmdlet 'in iş akışını başlattığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9148-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="c9148-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="c9148-113">-IndexRecommendationName</span></span>
<span data-ttu-id="c9148-114">Bu cmdlet 'in çalıştığı Dizin önerisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9148-114">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="c9148-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9148-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9148-116">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9148-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c9148-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9148-117">-ServerName</span></span>
<span data-ttu-id="c9148-118">Bu cmdlet 'in iş akışını başlattığı veritabanını barındıran sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9148-118">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="c9148-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9148-119">-DefaultProfile</span></span>
<span data-ttu-id="c9148-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9148-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9148-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9148-121">CommonParameters</span></span>
<span data-ttu-id="c9148-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9148-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9148-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9148-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9148-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9148-124">INPUTS</span></span>

## <span data-ttu-id="c9148-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9148-125">OUTPUTS</span></span>

## <span data-ttu-id="c9148-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9148-126">NOTES</span></span>

## <span data-ttu-id="c9148-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9148-127">RELATED LINKS</span></span>

[<span data-ttu-id="c9148-128">Get-Azurermsqldatabaseındexönerileri</span><span class="sxs-lookup"><span data-stu-id="c9148-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="c9148-129">Stop-Azurermsqldatabaseexecuteındexönerisi</span><span class="sxs-lookup"><span data-stu-id="c9148-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="c9148-130">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c9148-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


