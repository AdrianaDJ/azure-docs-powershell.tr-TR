---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096663"
---
# <span data-ttu-id="3a6a2-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="3a6a2-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="3a6a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6a2-103">Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğinden Add-AzAnalysisServicesAccount komutunda belirtilen bir günlüğü dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="3a6a2-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="3a6a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a6a2-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a6a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a6a2-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6a2-106">Export-AzAnalysisServicesInstance cmdlet 'i Azure Analysis Services sunucusundan dosyaya günlük aktarma</span><span class="sxs-lookup"><span data-stu-id="3a6a2-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="3a6a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a6a2-107">EXAMPLES</span></span>

### <span data-ttu-id="3a6a2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a6a2-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="3a6a2-109">Bu komut, Add-AzAnalysisServicesAccount komutunda belirtilen ortamdaki günlükleri ' TestServer ' sunucusundan dışarı aktarır ve bu dosyayı OutputPath ' C:\yol\to\log\testserver.log ' dosyasında belirtilen dosyaya kaydeder</span><span class="sxs-lookup"><span data-stu-id="3a6a2-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="3a6a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a6a2-110">PARAMETERS</span></span>

### <span data-ttu-id="3a6a2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3a6a2-111">-Force</span></span>
<span data-ttu-id="3a6a2-112">Varsa dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="3a6a2-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="3a6a2-113">-Örnek</span><span class="sxs-lookup"><span data-stu-id="3a6a2-113">-Instance</span></span>
<span data-ttu-id="3a6a2-114">Analysis Services sunucu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="3a6a2-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6a2-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="3a6a2-115">-OutputPath</span></span>
<span data-ttu-id="3a6a2-116">Dışarı aktarılacak dosyanın çıkış yolu</span><span class="sxs-lookup"><span data-stu-id="3a6a2-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="3a6a2-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a6a2-117">-PassThru</span></span>
<span data-ttu-id="3a6a2-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="3a6a2-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3a6a2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a6a2-119">-Confirm</span></span>
<span data-ttu-id="3a6a2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a6a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6a2-121">-WhatIf</span></span>
<span data-ttu-id="3a6a2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a6a2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6a2-124">CommonParameters</span></span>
<span data-ttu-id="3a6a2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6a2-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6a2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6a2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a6a2-127">INPUTS</span></span>

### <span data-ttu-id="3a6a2-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3a6a2-128">None</span></span>

## <span data-ttu-id="3a6a2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a6a2-129">OUTPUTS</span></span>

### <span data-ttu-id="3a6a2-130">System. void</span><span class="sxs-lookup"><span data-stu-id="3a6a2-130">System.Void</span></span>

## <span data-ttu-id="3a6a2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a6a2-131">NOTES</span></span>
<span data-ttu-id="3a6a2-132">Diğer ad: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="3a6a2-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="3a6a2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a6a2-133">RELATED LINKS</span></span>
