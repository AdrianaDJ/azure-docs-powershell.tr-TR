---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 04a1c63ac2ae1b0db692f2bef4b4803a8acb744f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751217"
---
# <span data-ttu-id="c604c-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c604c-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="c604c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c604c-102">SYNOPSIS</span></span>
<span data-ttu-id="c604c-103">Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğinden Add-AzAnalysisServicesAccount komutunda belirtilen bir günlüğü dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="c604c-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c604c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c604c-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c604c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c604c-105">DESCRIPTION</span></span>
<span data-ttu-id="c604c-106">Export-AzAnalysisServicesInstance cmdlet 'i Azure Analysis Services sunucusundan dosyaya günlük aktarma</span><span class="sxs-lookup"><span data-stu-id="c604c-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="c604c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c604c-107">EXAMPLES</span></span>

### <span data-ttu-id="c604c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c604c-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="c604c-109">Bu komut, Add-AzAnalysisServicesAccount komutunda belirtilen ortamdaki günlükleri ' TestServer ' sunucusundan dışarı aktarır ve bu dosyayı OutputPath ' C:\yol\to\log\testserver.log ' dosyasında belirtilen dosyaya kaydeder</span><span class="sxs-lookup"><span data-stu-id="c604c-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="c604c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c604c-110">PARAMETERS</span></span>

### <span data-ttu-id="c604c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c604c-111">-Force</span></span>
<span data-ttu-id="c604c-112">Varsa dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="c604c-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="c604c-113">-Örnek</span><span class="sxs-lookup"><span data-stu-id="c604c-113">-Instance</span></span>
<span data-ttu-id="c604c-114">Analysis Services sunucu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="c604c-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="c604c-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c604c-115">-OutputPath</span></span>
<span data-ttu-id="c604c-116">Dışarı aktarılacak dosyanın çıkış yolu</span><span class="sxs-lookup"><span data-stu-id="c604c-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="c604c-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c604c-117">-PassThru</span></span>
<span data-ttu-id="c604c-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c604c-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c604c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c604c-119">-Confirm</span></span>
<span data-ttu-id="c604c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c604c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c604c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c604c-121">-WhatIf</span></span>
<span data-ttu-id="c604c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c604c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c604c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c604c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c604c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c604c-124">CommonParameters</span></span>
<span data-ttu-id="c604c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c604c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c604c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c604c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c604c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c604c-127">INPUTS</span></span>

### <span data-ttu-id="c604c-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c604c-128">None</span></span>

## <span data-ttu-id="c604c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c604c-129">OUTPUTS</span></span>

### <span data-ttu-id="c604c-130">System. void</span><span class="sxs-lookup"><span data-stu-id="c604c-130">System.Void</span></span>

## <span data-ttu-id="c604c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c604c-131">NOTES</span></span>
<span data-ttu-id="c604c-132">Diğer ad: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="c604c-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="c604c-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c604c-133">RELATED LINKS</span></span>
