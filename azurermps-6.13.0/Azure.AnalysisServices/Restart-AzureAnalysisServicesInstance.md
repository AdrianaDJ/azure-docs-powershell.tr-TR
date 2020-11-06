---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 496c0410808604303ab60d8ad4d989e838828bf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587373"
---
# <span data-ttu-id="c6b4b-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="c6b4b-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="c6b4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b4b-103">Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğini Add-AzureAnalysisServicesAccount komutunda belirtildiği gibi yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="c6b4b-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6b4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6b4b-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance -Instance <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6b4b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b4b-106">Restart-AzureAnalysisServicesInstance cmdlet 'i yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="c6b4b-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="c6b4b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6b4b-107">EXAMPLES</span></span>

### <span data-ttu-id="c6b4b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6b4b-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="c6b4b-109">Bu komut, Add-AzureAnalysisServicesAccount komutunda belirtilen ortamda ' TestServer ' sunucusunu yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="c6b4b-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="c6b4b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6b4b-110">PARAMETERS</span></span>

### <span data-ttu-id="c6b4b-111">-Örnek</span><span class="sxs-lookup"><span data-stu-id="c6b4b-111">-Instance</span></span>
<span data-ttu-id="c6b4b-112">Yeniden başlatılacak Analysis Services sunucusu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="c6b4b-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="c6b4b-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c6b4b-113">-PassThru</span></span>
<span data-ttu-id="c6b4b-114">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="c6b4b-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c6b4b-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6b4b-115">-Confirm</span></span>
<span data-ttu-id="c6b4b-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6b4b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b4b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b4b-117">-WhatIf</span></span>
<span data-ttu-id="c6b4b-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6b4b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b4b-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6b4b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b4b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b4b-120">CommonParameters</span></span>
<span data-ttu-id="c6b4b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6b4b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b4b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6b4b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b4b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6b4b-123">INPUTS</span></span>

### <span data-ttu-id="c6b4b-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c6b4b-124">None</span></span>

## <span data-ttu-id="c6b4b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6b4b-125">OUTPUTS</span></span>

### <span data-ttu-id="c6b4b-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6b4b-126">System.Boolean</span></span>

## <span data-ttu-id="c6b4b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6b4b-127">NOTES</span></span>
<span data-ttu-id="c6b4b-128">Diğer ad: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="c6b4b-128">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="c6b4b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6b4b-129">RELATED LINKS</span></span>
