---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765071"
---
# <span data-ttu-id="a657d-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="a657d-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="a657d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a657d-102">SYNOPSIS</span></span>
<span data-ttu-id="a657d-103">Şu anda oturum açmış olan ortamdaki bir Analysis Services sunucusu örneğinden Add-AzureAnalysisServicesAccount komutunda belirtilen bir günlüğü dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="a657d-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a657d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a657d-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="a657d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a657d-105">DESCRIPTION</span></span>
<span data-ttu-id="a657d-106">Export-AzureAnalysisServicesInstance cmdlet 'i Azure Analysis Services sunucusundan dosyaya günlük aktarma</span><span class="sxs-lookup"><span data-stu-id="a657d-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="a657d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a657d-107">EXAMPLES</span></span>

### <span data-ttu-id="a657d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a657d-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="a657d-109">Bu komut, Add-AzureAnalysisServicesAccount komutunda belirtilen ortamdaki günlükleri ' TestServer ' sunucusundan dışarı aktarır ve bu dosyayı OutputPath ' C:\yol\to\log\testserver.log ' dosyasında belirtilen dosyaya kaydeder</span><span class="sxs-lookup"><span data-stu-id="a657d-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="a657d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a657d-110">PARAMETERS</span></span>

### <span data-ttu-id="a657d-111">-Örnek</span><span class="sxs-lookup"><span data-stu-id="a657d-111">-Instance</span></span>
<span data-ttu-id="a657d-112">Analysis Services sunucu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="a657d-112">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="a657d-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a657d-113">-OutputPath</span></span>
<span data-ttu-id="a657d-114">Dışarı aktarılacak dosyanın çıkış yolu</span><span class="sxs-lookup"><span data-stu-id="a657d-114">Output path to file to export log</span></span>

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

### <span data-ttu-id="a657d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a657d-115">-Force</span></span>
<span data-ttu-id="a657d-116">Varsa dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="a657d-116">Overwrite file if exists without asking</span></span>

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

## <span data-ttu-id="a657d-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a657d-117">INPUTS</span></span>

## <span data-ttu-id="a657d-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a657d-118">OUTPUTS</span></span>

## <span data-ttu-id="a657d-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a657d-119">NOTES</span></span>
<span data-ttu-id="a657d-120">Diğer ad: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a657d-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="a657d-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a657d-121">RELATED LINKS</span></span>

