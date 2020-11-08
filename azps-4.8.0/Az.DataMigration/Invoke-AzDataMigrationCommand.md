---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267772"
---
# <span data-ttu-id="24f4d-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="24f4d-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="24f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="24f4d-103">Var olan bir DMS görevinde yürütülecek yeni bir komut oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24f4d-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="24f4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24f4d-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="24f4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="24f4d-106">Invoke-AzDataMigrationCommand cmdlet, var olan geçiş görevinde çalıştırılacak yeni bir komut görevi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24f4d-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="24f4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24f4d-107">EXAMPLES</span></span>

### <span data-ttu-id="24f4d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24f4d-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="24f4d-109">Yukarıdaki örneklerde, var olan hizmet, proje ve görev için komut oluşturmak için Invoke-AzDataMigrationCommand cmdlet 'i kullanılır</span><span class="sxs-lookup"><span data-stu-id="24f4d-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="24f4d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24f4d-110">PARAMETERS</span></span>

### <span data-ttu-id="24f4d-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="24f4d-111">-CommandType</span></span>
<span data-ttu-id="24f4d-112">Komut türü.</span><span class="sxs-lookup"><span data-stu-id="24f4d-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f4d-113">-DefaultProfile</span></span>
<span data-ttu-id="24f4d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24f4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f4d-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="24f4d-115">-ProjectName</span></span>
<span data-ttu-id="24f4d-116">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="24f4d-116">The name of the project.</span></span>

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

### <span data-ttu-id="24f4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="24f4d-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="24f4d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="24f4d-119">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="24f4d-119">-ServiceName</span></span>
<span data-ttu-id="24f4d-120">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="24f4d-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="24f4d-121">-GörevAdı</span><span class="sxs-lookup"><span data-stu-id="24f4d-121">-TaskName</span></span>
<span data-ttu-id="24f4d-122">Komutun üzerinde çalışacağı görevin adı.</span><span class="sxs-lookup"><span data-stu-id="24f4d-122">The name of the task the command is run on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="24f4d-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="24f4d-123">-ObjectName</span></span>
<span data-ttu-id="24f4d-124">Komutun çalışacağı veritabanı nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="24f4d-124">The name of the database object the command will run against.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f4d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="24f4d-125">-Confirm</span></span>
<span data-ttu-id="24f4d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24f4d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f4d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f4d-127">-WhatIf</span></span>
<span data-ttu-id="24f4d-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24f4d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f4d-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24f4d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f4d-130">CommonParameters</span></span>
<span data-ttu-id="24f4d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24f4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f4d-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f4d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f4d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24f4d-133">INPUTS</span></span>

### <span data-ttu-id="24f4d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="24f4d-134">System.String</span></span>

## <span data-ttu-id="24f4d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24f4d-135">OUTPUTS</span></span>

### <span data-ttu-id="24f4d-136">Microsoft. Azure. Management. DataMigration. modeller. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="24f4d-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="24f4d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24f4d-137">NOTES</span></span>

## <span data-ttu-id="24f4d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24f4d-138">RELATED LINKS</span></span>
