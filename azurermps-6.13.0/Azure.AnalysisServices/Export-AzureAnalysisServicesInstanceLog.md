---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588669"
---
# <span data-ttu-id="97895-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="97895-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="97895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97895-102">SYNOPSIS</span></span>
<span data-ttu-id="97895-103">Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğinden Add-AzureAnalysisServicesAccount komutunda belirtilen bir günlüğü dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="97895-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97895-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97895-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97895-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97895-105">DESCRIPTION</span></span>
<span data-ttu-id="97895-106">Export-AzureAnalysisServicesInstance cmdlet 'i Azure Analysis Services sunucusundan dosyaya günlük aktarma</span><span class="sxs-lookup"><span data-stu-id="97895-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="97895-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97895-107">EXAMPLES</span></span>

### <span data-ttu-id="97895-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="97895-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="97895-109">Bu komut, Add-AzureAnalysisServicesAccount komutunda belirtilen ortamdaki günlükleri ' TestServer ' sunucusundan dışarı aktarır ve bu dosyayı OutputPath ' C:\yol\to\log\testserver.log ' dosyasında belirtilen dosyaya kaydeder</span><span class="sxs-lookup"><span data-stu-id="97895-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="97895-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97895-110">PARAMETERS</span></span>

### <span data-ttu-id="97895-111">-Force</span><span class="sxs-lookup"><span data-stu-id="97895-111">-Force</span></span>
<span data-ttu-id="97895-112">Varsa dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="97895-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="97895-113">-Örnek</span><span class="sxs-lookup"><span data-stu-id="97895-113">-Instance</span></span>
<span data-ttu-id="97895-114">Analysis Services sunucu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="97895-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="97895-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="97895-115">-OutputPath</span></span>
<span data-ttu-id="97895-116">Dışarı aktarılacak dosyanın çıkış yolu</span><span class="sxs-lookup"><span data-stu-id="97895-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="97895-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="97895-117">-Confirm</span></span>
<span data-ttu-id="97895-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97895-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97895-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97895-119">-WhatIf</span></span>
<span data-ttu-id="97895-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97895-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97895-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97895-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97895-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97895-122">CommonParameters</span></span>
<span data-ttu-id="97895-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97895-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97895-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97895-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97895-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97895-125">INPUTS</span></span>

### <span data-ttu-id="97895-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="97895-126">None</span></span>

## <span data-ttu-id="97895-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97895-127">OUTPUTS</span></span>

### <span data-ttu-id="97895-128">System. void</span><span class="sxs-lookup"><span data-stu-id="97895-128">System.Void</span></span>

## <span data-ttu-id="97895-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97895-129">NOTES</span></span>
<span data-ttu-id="97895-130">Diğer ad: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="97895-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="97895-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97895-131">RELATED LINKS</span></span>
