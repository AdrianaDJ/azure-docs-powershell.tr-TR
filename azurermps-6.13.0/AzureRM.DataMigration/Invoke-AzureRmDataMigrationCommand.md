---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591970"
---
# <span data-ttu-id="8f992-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="8f992-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="8f992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f992-102">SYNOPSIS</span></span>
<span data-ttu-id="8f992-103">Var olan bir DMS görevinde yürütülecek yeni bir komut oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f992-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f992-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f992-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f992-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f992-105">DESCRIPTION</span></span>
<span data-ttu-id="8f992-106">New-AzureRmDataMigrationCommand cmdlet, var olan geçiş görevinde çalıştırılacak yeni bir komut görevi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f992-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="8f992-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f992-107">EXAMPLES</span></span>

### <span data-ttu-id="8f992-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8f992-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="8f992-109">Yukarıdaki örneklerde, var olan hizmet, proje ve görev için komut oluşturmak için New-AzureRmDmsCommand cmdlet 'i kullanılır</span><span class="sxs-lookup"><span data-stu-id="8f992-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="8f992-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f992-110">PARAMETERS</span></span>

### <span data-ttu-id="8f992-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="8f992-111">-CommandType</span></span>
<span data-ttu-id="8f992-112">Komut türü.</span><span class="sxs-lookup"><span data-stu-id="8f992-112">Command Type.</span></span>

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

### <span data-ttu-id="8f992-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f992-113">-DefaultProfile</span></span>
<span data-ttu-id="8f992-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f992-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f992-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="8f992-115">-ProjectName</span></span>
<span data-ttu-id="8f992-116">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="8f992-116">The name of the project.</span></span>

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

### <span data-ttu-id="8f992-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f992-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f992-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8f992-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f992-119">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="8f992-119">-ServiceName</span></span>
<span data-ttu-id="8f992-120">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="8f992-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8f992-121">-GörevAdı</span><span class="sxs-lookup"><span data-stu-id="8f992-121">-TaskName</span></span>
<span data-ttu-id="8f992-122">Komutun üzerinde çalışacağı görevin adı.</span><span class="sxs-lookup"><span data-stu-id="8f992-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="8f992-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f992-123">-Confirm</span></span>
<span data-ttu-id="8f992-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f992-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f992-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f992-125">-WhatIf</span></span>
<span data-ttu-id="8f992-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f992-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f992-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f992-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f992-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f992-128">CommonParameters</span></span>
<span data-ttu-id="8f992-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f992-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f992-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f992-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f992-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f992-131">INPUTS</span></span>

### <span data-ttu-id="8f992-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f992-132">System.String</span></span>

## <span data-ttu-id="8f992-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f992-133">OUTPUTS</span></span>

### <span data-ttu-id="8f992-134">Microsoft. Azure. Management. DataMigration. modeller. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="8f992-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="8f992-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f992-135">NOTES</span></span>

## <span data-ttu-id="8f992-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f992-136">RELATED LINKS</span></span>
