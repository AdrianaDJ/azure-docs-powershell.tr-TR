---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f4f3b935aa9303ab38888d6f28f0a89bbdeb6c23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758734"
---
# <span data-ttu-id="6e451-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="6e451-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="6e451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e451-102">SYNOPSIS</span></span>
<span data-ttu-id="6e451-103">Veritabanındaki zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="6e451-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="6e451-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e451-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e451-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e451-105">DESCRIPTION</span></span>
<span data-ttu-id="6e451-106">**Stop-AzSqlDatabaseActivity** cmdlet 'i veritabanındaki zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="6e451-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="6e451-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e451-107">EXAMPLES</span></span>

### <span data-ttu-id="6e451-108">Örnek 1: veritabanındaki zaman uyumsuz güncelleştirmeler işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="6e451-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="6e451-109">Bu komut, veritabanındaki zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="6e451-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="6e451-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e451-110">PARAMETERS</span></span>

### <span data-ttu-id="6e451-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e451-111">-DatabaseName</span></span>
<span data-ttu-id="6e451-112">Bu cmdlet 'in durumu aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e451-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="6e451-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e451-113">-DefaultProfile</span></span>
<span data-ttu-id="6e451-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e451-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e451-115">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="6e451-115">-ElasticPoolName</span></span>
<span data-ttu-id="6e451-116">Azure SQL esnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="6e451-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="6e451-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6e451-117">-OperationId</span></span>
<span data-ttu-id="6e451-118">Bu cmdlet 'in aldığı işlemin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e451-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e451-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e451-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e451-120">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e451-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="6e451-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e451-121">-ServerName</span></span>
<span data-ttu-id="6e451-122">Veritabanını barındıran Microsoft SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e451-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e451-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e451-123">-Confirm</span></span>
<span data-ttu-id="6e451-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e451-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e451-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e451-125">-WhatIf</span></span>
<span data-ttu-id="6e451-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e451-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e451-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e451-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e451-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e451-128">CommonParameters</span></span>
<span data-ttu-id="6e451-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e451-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e451-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e451-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e451-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e451-131">INPUTS</span></span>

### <span data-ttu-id="6e451-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6e451-132">System.String</span></span>

### <span data-ttu-id="6e451-133">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="6e451-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6e451-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e451-134">OUTPUTS</span></span>

### <span data-ttu-id="6e451-135">Microsoft. Azure. Commands. Sql. Database. model. azures, Databaseactivitymodel</span><span class="sxs-lookup"><span data-stu-id="6e451-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="6e451-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e451-136">NOTES</span></span>

## <span data-ttu-id="6e451-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e451-137">RELATED LINKS</span></span>