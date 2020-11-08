---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 0082918e09c0f42910ead42d03319577d4b4c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933937"
---
# <span data-ttu-id="2cb29-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2cb29-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="2cb29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cb29-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb29-103">Esnek havuzda zaman uyumsuz güncelleştirme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="2cb29-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="2cb29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cb29-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cb29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cb29-105">DESCRIPTION</span></span>
<span data-ttu-id="2cb29-106">**Stop-AzSqlElasticPoolActivity** cmdlet 'i, esnek havuzda zaman uyumsuz güncelleştirme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="2cb29-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="2cb29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cb29-107">EXAMPLES</span></span>

### <span data-ttu-id="2cb29-108">Örnek 1: esnek havuzda zaman uyumsuz güncelleştirme işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="2cb29-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="2cb29-109">Bu komut, esnek havuzda zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="2cb29-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="2cb29-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cb29-110">PARAMETERS</span></span>

### <span data-ttu-id="2cb29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb29-111">-DefaultProfile</span></span>
<span data-ttu-id="2cb29-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cb29-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cb29-113">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="2cb29-113">-ElasticPoolName</span></span>
<span data-ttu-id="2cb29-114">Azure SQL esnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="2cb29-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb29-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2cb29-115">-OperationId</span></span>
<span data-ttu-id="2cb29-116">Alınacak işlemin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2cb29-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="2cb29-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2cb29-117">-PassThru</span></span>
<span data-ttu-id="2cb29-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2cb29-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb29-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb29-119">-ResourceGroupName</span></span>
<span data-ttu-id="2cb29-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2cb29-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2cb29-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2cb29-121">-ServerName</span></span>
<span data-ttu-id="2cb29-122">Elastik havuzun bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="2cb29-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="2cb29-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2cb29-123">-Confirm</span></span>
<span data-ttu-id="2cb29-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2cb29-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb29-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cb29-125">-WhatIf</span></span>
<span data-ttu-id="2cb29-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cb29-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cb29-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2cb29-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb29-128">CommonParameters</span></span>
<span data-ttu-id="2cb29-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cb29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb29-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2cb29-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb29-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cb29-131">INPUTS</span></span>

### <span data-ttu-id="2cb29-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2cb29-132">System.String</span></span>

### <span data-ttu-id="2cb29-133">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="2cb29-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2cb29-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cb29-134">OUTPUTS</span></span>

### <span data-ttu-id="2cb29-135">Microsoft. Azure. Commands. Sql. Elaçıkartma. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="2cb29-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="2cb29-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cb29-136">NOTES</span></span>

## <span data-ttu-id="2cb29-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cb29-137">RELATED LINKS</span></span>