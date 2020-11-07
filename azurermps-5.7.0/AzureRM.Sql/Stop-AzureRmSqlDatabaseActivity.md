---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: d0aa42b8b584ade698c3d03848a537350ac342d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763208"
---
# <span data-ttu-id="7276c-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="7276c-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="7276c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7276c-102">SYNOPSIS</span></span>
<span data-ttu-id="7276c-103">Veritabanındaki zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="7276c-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7276c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7276c-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7276c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7276c-105">DESCRIPTION</span></span>
<span data-ttu-id="7276c-106">**Stop-AzureRmSqlDatabaseActivity** cmdlet 'i veritabanındaki zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="7276c-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7276c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7276c-107">EXAMPLES</span></span>

### <span data-ttu-id="7276c-108">Örnek 1: veritabanındaki zaman uyumsuz güncelleştirmeler işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="7276c-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="7276c-109">Bu komut, veritabanındaki zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="7276c-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7276c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7276c-110">PARAMETERS</span></span>

### <span data-ttu-id="7276c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7276c-111">-DatabaseName</span></span>
<span data-ttu-id="7276c-112">Bu cmdlet 'in durumu aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7276c-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="7276c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7276c-113">-DefaultProfile</span></span>
<span data-ttu-id="7276c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7276c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7276c-115">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="7276c-115">-ElasticPoolName</span></span>
<span data-ttu-id="7276c-116">Azure SQL esnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="7276c-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7276c-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7276c-117">-OperationId</span></span>
<span data-ttu-id="7276c-118">Bu cmdlet 'in aldığı işlemin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7276c-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7276c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7276c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7276c-120">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7276c-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7276c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7276c-121">-ServerName</span></span>
<span data-ttu-id="7276c-122">Veritabanını barındıran Microsoft SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7276c-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7276c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="7276c-123">-Confirm</span></span>
<span data-ttu-id="7276c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7276c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7276c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7276c-125">-WhatIf</span></span>
<span data-ttu-id="7276c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7276c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7276c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7276c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7276c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7276c-128">CommonParameters</span></span>
<span data-ttu-id="7276c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7276c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7276c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7276c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7276c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7276c-131">INPUTS</span></span>

### <span data-ttu-id="7276c-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7276c-132">None</span></span>
<span data-ttu-id="7276c-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7276c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7276c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7276c-134">OUTPUTS</span></span>

### <span data-ttu-id="7276c-135">Microsoft. Azure. Commands. Sql. Database. model. azures, Databaseactivitymodel</span><span class="sxs-lookup"><span data-stu-id="7276c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="7276c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7276c-136">NOTES</span></span>

## <span data-ttu-id="7276c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7276c-137">RELATED LINKS</span></span>
