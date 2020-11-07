---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 4d4e2a86bfa2974cabcc4208f7a314019f5804e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753673"
---
# <span data-ttu-id="c0751-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="c0751-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="c0751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0751-102">SYNOPSIS</span></span>
<span data-ttu-id="c0751-103">Start-AzKubernetesDashboard 'de oluşturulan Kubectl SSH tünelini durdurun.</span><span class="sxs-lookup"><span data-stu-id="c0751-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="c0751-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0751-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0751-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0751-105">DESCRIPTION</span></span>
<span data-ttu-id="c0751-106">Start-AzKubernetesDashboard 'de oluşturulan Kubectl SSH tünelini durdurun.</span><span class="sxs-lookup"><span data-stu-id="c0751-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="c0751-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0751-107">EXAMPLES</span></span>

### <span data-ttu-id="c0751-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0751-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="c0751-109">Start-AzKubernetesDashboard 'i yürüterek mevcut SSH tüneli kurulumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="c0751-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="c0751-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0751-110">PARAMETERS</span></span>

### <span data-ttu-id="c0751-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0751-111">-DefaultProfile</span></span>
<span data-ttu-id="c0751-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0751-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0751-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c0751-113">-PassThru</span></span>
<span data-ttu-id="c0751-114">SSH tüneli kapalıysa doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0751-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="c0751-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0751-115">CommonParameters</span></span>
<span data-ttu-id="c0751-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0751-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0751-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0751-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0751-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0751-118">INPUTS</span></span>

### <span data-ttu-id="c0751-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c0751-119">None</span></span>

## <span data-ttu-id="c0751-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0751-120">OUTPUTS</span></span>

### <span data-ttu-id="c0751-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0751-121">System.Boolean</span></span>

## <span data-ttu-id="c0751-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0751-122">NOTES</span></span>

## <span data-ttu-id="c0751-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0751-123">RELATED LINKS</span></span>
