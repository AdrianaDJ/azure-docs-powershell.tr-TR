---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 1f7306d78d7c0405929ba7dae2512b141a4f4a89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751328"
---
# <span data-ttu-id="64bc1-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="64bc1-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="64bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="64bc1-103">Günlük profili alır.</span><span class="sxs-lookup"><span data-stu-id="64bc1-103">Gets a log profile.</span></span>

## <span data-ttu-id="64bc1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64bc1-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64bc1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64bc1-105">DESCRIPTION</span></span>
<span data-ttu-id="64bc1-106">**Get-AzLogProfile** cmdlet 'i bir günlük profili alır.</span><span class="sxs-lookup"><span data-stu-id="64bc1-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="64bc1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64bc1-107">EXAMPLES</span></span>

## <span data-ttu-id="64bc1-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64bc1-108">PARAMETERS</span></span>

### <span data-ttu-id="64bc1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64bc1-109">-DefaultProfile</span></span>
<span data-ttu-id="64bc1-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="64bc1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64bc1-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="64bc1-111">-Name</span></span>
<span data-ttu-id="64bc1-112">Alınacak günlük profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64bc1-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64bc1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64bc1-113">CommonParameters</span></span>
<span data-ttu-id="64bc1-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64bc1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64bc1-115">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="64bc1-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64bc1-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64bc1-116">INPUTS</span></span>

### <span data-ttu-id="64bc1-117">System. String</span><span class="sxs-lookup"><span data-stu-id="64bc1-117">System.String</span></span>

## <span data-ttu-id="64bc1-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64bc1-118">OUTPUTS</span></span>

### <span data-ttu-id="64bc1-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="64bc1-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="64bc1-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64bc1-120">NOTES</span></span>

## <span data-ttu-id="64bc1-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64bc1-121">RELATED LINKS</span></span>

[<span data-ttu-id="64bc1-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="64bc1-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="64bc1-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="64bc1-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


