---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097523"
---
# <span data-ttu-id="43007-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="43007-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="43007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43007-102">SYNOPSIS</span></span>
<span data-ttu-id="43007-103">Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğini Add-AzAnalysisServicesAccount komutunda belirtildiği gibi yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="43007-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="43007-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43007-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43007-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43007-105">DESCRIPTION</span></span>
<span data-ttu-id="43007-106">Restart-AzAnalysisServicesInstance cmdlet 'i yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="43007-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="43007-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43007-107">EXAMPLES</span></span>

### <span data-ttu-id="43007-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="43007-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="43007-109">Bu komut, Add-AzAnalysisServicesAccount komutunda belirtilen ortamda ' TestServer ' sunucusunu yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="43007-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="43007-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43007-110">PARAMETERS</span></span>

### <span data-ttu-id="43007-111">-Örnek</span><span class="sxs-lookup"><span data-stu-id="43007-111">-Instance</span></span>
<span data-ttu-id="43007-112">Yeniden başlatılacak Analysis Services sunucusu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="43007-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="43007-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="43007-113">-PassThru</span></span>
<span data-ttu-id="43007-114">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="43007-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="43007-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="43007-115">-Confirm</span></span>
<span data-ttu-id="43007-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43007-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43007-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43007-117">-WhatIf</span></span>
<span data-ttu-id="43007-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43007-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43007-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43007-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43007-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43007-120">CommonParameters</span></span>
<span data-ttu-id="43007-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43007-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43007-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43007-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43007-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43007-123">INPUTS</span></span>

### <span data-ttu-id="43007-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="43007-124">None</span></span>

## <span data-ttu-id="43007-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43007-125">OUTPUTS</span></span>

### <span data-ttu-id="43007-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43007-126">System.Boolean</span></span>

## <span data-ttu-id="43007-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43007-127">NOTES</span></span>
<span data-ttu-id="43007-128">Diğer ad: Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="43007-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="43007-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43007-129">RELATED LINKS</span></span>