---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 87744454627feaadc8c953e1ad4e50016f14879f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592381"
---
# <span data-ttu-id="9cefe-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="9cefe-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="9cefe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cefe-102">SYNOPSIS</span></span>
<span data-ttu-id="9cefe-103">Esnek havuzda zaman uyumsuz güncelleştirme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="9cefe-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cefe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cefe-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cefe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cefe-105">DESCRIPTION</span></span>
<span data-ttu-id="9cefe-106">**Stop-AzureRmSqlElasticPoolActivity** cmdlet 'i, esnek havuzda zaman uyumsuz güncelleştirme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="9cefe-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="9cefe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cefe-107">EXAMPLES</span></span>

### <span data-ttu-id="9cefe-108">Örnek 1: esnek havuzda zaman uyumsuz güncelleştirme işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="9cefe-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="9cefe-109">Bu komut, esnek havuzda zaman uyumsuz güncelleştirmeler işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="9cefe-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="9cefe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cefe-110">PARAMETERS</span></span>

### <span data-ttu-id="9cefe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cefe-111">-DefaultProfile</span></span>
<span data-ttu-id="9cefe-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cefe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cefe-113">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="9cefe-113">-ElasticPoolName</span></span>
<span data-ttu-id="9cefe-114">Azure SQL esnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="9cefe-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cefe-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9cefe-115">-OperationId</span></span>
<span data-ttu-id="9cefe-116">Alınacak işlemin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9cefe-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="9cefe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cefe-117">-ResourceGroupName</span></span>
<span data-ttu-id="9cefe-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9cefe-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9cefe-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9cefe-119">-ServerName</span></span>
<span data-ttu-id="9cefe-120">Elastik havuzun bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="9cefe-120">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="9cefe-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cefe-121">-Confirm</span></span>
<span data-ttu-id="9cefe-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cefe-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cefe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cefe-123">-WhatIf</span></span>
<span data-ttu-id="9cefe-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cefe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cefe-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cefe-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cefe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cefe-126">CommonParameters</span></span>
<span data-ttu-id="9cefe-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cefe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cefe-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cefe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cefe-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cefe-129">INPUTS</span></span>

### <span data-ttu-id="9cefe-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9cefe-130">None</span></span>

<span data-ttu-id="9cefe-131">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cefe-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="9cefe-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cefe-132">OUTPUTS</span></span>

### <span data-ttu-id="9cefe-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="9cefe-133">System.Object</span></span>

## <span data-ttu-id="9cefe-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cefe-134">NOTES</span></span>

## <span data-ttu-id="9cefe-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cefe-135">RELATED LINKS</span></span>



