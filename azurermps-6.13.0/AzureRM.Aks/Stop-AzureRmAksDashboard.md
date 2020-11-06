---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 719ef5fd3676fdc5d5b6b8460bcb3edafabb83f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589629"
---
# <span data-ttu-id="2ecb5-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="2ecb5-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="2ecb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ecb5-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecb5-103">Start-AzureRmKubernetesDashboard 'de oluşturulan Kubectl SSH tünelini durdurun.</span><span class="sxs-lookup"><span data-stu-id="2ecb5-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ecb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ecb5-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ecb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ecb5-105">DESCRIPTION</span></span>
<span data-ttu-id="2ecb5-106">Start-AzureRmKubernetesDashboard 'de oluşturulan Kubectl SSH tünelini durdurun.</span><span class="sxs-lookup"><span data-stu-id="2ecb5-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="2ecb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ecb5-107">EXAMPLES</span></span>

### <span data-ttu-id="2ecb5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ecb5-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="2ecb5-109">Start-AzureRmKubernetesDashboard 'i yürüterek mevcut SSH tüneli kurulumunu durdurur.</span><span class="sxs-lookup"><span data-stu-id="2ecb5-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="2ecb5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ecb5-110">PARAMETERS</span></span>

### <span data-ttu-id="2ecb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecb5-111">-DefaultProfile</span></span>
<span data-ttu-id="2ecb5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ecb5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ecb5-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ecb5-113">-PassThru</span></span>
<span data-ttu-id="2ecb5-114">SSH tüneli kapalıysa doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ecb5-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="2ecb5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecb5-115">CommonParameters</span></span>
<span data-ttu-id="2ecb5-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ecb5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecb5-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ecb5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecb5-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ecb5-118">INPUTS</span></span>

### <span data-ttu-id="2ecb5-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2ecb5-119">None</span></span>

## <span data-ttu-id="2ecb5-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ecb5-120">OUTPUTS</span></span>

### <span data-ttu-id="2ecb5-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ecb5-121">System.Boolean</span></span>

## <span data-ttu-id="2ecb5-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ecb5-122">NOTES</span></span>

## <span data-ttu-id="2ecb5-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ecb5-123">RELATED LINKS</span></span>
