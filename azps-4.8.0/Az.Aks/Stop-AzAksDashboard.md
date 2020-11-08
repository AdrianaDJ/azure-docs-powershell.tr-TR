---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266159"
---
# <span data-ttu-id="d709e-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="d709e-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="d709e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d709e-102">SYNOPSIS</span></span>
<span data-ttu-id="d709e-103">Start-AzKubernetesDashboard 'de oluşturulan Kubectl SSH tünelini durdurun.</span><span class="sxs-lookup"><span data-stu-id="d709e-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d709e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d709e-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d709e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d709e-105">DESCRIPTION</span></span>
<span data-ttu-id="d709e-106">Start-AzKubernetesDashboard 'de oluşturulan Kubectl SSH tünelini durdurun.</span><span class="sxs-lookup"><span data-stu-id="d709e-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d709e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d709e-107">EXAMPLES</span></span>

### <span data-ttu-id="d709e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d709e-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="d709e-109">Start-AzKubernetesDashboard 'i yürüterek mevcut SSH tüneli kurulumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="d709e-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d709e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d709e-110">PARAMETERS</span></span>

### <span data-ttu-id="d709e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d709e-111">-DefaultProfile</span></span>
<span data-ttu-id="d709e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d709e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d709e-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d709e-113">-PassThru</span></span>
<span data-ttu-id="d709e-114">SSH tüneli kapalıysa doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="d709e-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="d709e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d709e-115">CommonParameters</span></span>
<span data-ttu-id="d709e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d709e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d709e-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d709e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d709e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d709e-118">INPUTS</span></span>

### <span data-ttu-id="d709e-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d709e-119">None</span></span>

## <span data-ttu-id="d709e-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d709e-120">OUTPUTS</span></span>

### <span data-ttu-id="d709e-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d709e-121">System.Boolean</span></span>

## <span data-ttu-id="d709e-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d709e-122">NOTES</span></span>

## <span data-ttu-id="d709e-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d709e-123">RELATED LINKS</span></span>
