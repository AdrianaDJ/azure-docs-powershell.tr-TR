---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/restart-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 0a89ee592e6f6f6d4d9e56df6d7e4df32b010524
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590546"
---
# <span data-ttu-id="99ab7-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="99ab7-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="99ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="99ab7-103">Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğini Add-AzureAnalysisServicesAccount komutunda belirtildiği gibi yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="99ab7-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99ab7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99ab7-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="99ab7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="99ab7-106">Restart-AzureAnalysisServicesInstance cmdlet 'i yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="99ab7-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="99ab7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99ab7-107">EXAMPLES</span></span>

### <span data-ttu-id="99ab7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99ab7-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="99ab7-109">Bu komut, Add-AzureAnalysisServicesAccount komutunda belirtilen ortamda ' TestServer ' sunucusunu yeniden başlatır</span><span class="sxs-lookup"><span data-stu-id="99ab7-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="99ab7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99ab7-110">PARAMETERS</span></span>

### <span data-ttu-id="99ab7-111">-Örnek</span><span class="sxs-lookup"><span data-stu-id="99ab7-111">-Instance</span></span>
<span data-ttu-id="99ab7-112">Yeniden başlatılacak Analysis Services sunucusu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="99ab7-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ab7-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="99ab7-113">-PassThru</span></span>
<span data-ttu-id="99ab7-114">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="99ab7-114">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ab7-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="99ab7-115">-Confirm</span></span>
<span data-ttu-id="99ab7-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99ab7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ab7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ab7-117">-WhatIf</span></span>
<span data-ttu-id="99ab7-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99ab7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ab7-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99ab7-119">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="99ab7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99ab7-120">INPUTS</span></span>

### <span data-ttu-id="99ab7-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="99ab7-121">None</span></span>
<span data-ttu-id="99ab7-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="99ab7-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99ab7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99ab7-123">OUTPUTS</span></span>

### <span data-ttu-id="99ab7-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99ab7-124">System.Boolean</span></span>

## <span data-ttu-id="99ab7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99ab7-125">NOTES</span></span>
<span data-ttu-id="99ab7-126">Diğer ad: Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="99ab7-126">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="99ab7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99ab7-127">RELATED LINKS</span></span>

