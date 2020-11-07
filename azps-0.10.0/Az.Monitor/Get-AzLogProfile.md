---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 5d99bafdd011409eae322c60db6e596d3c77cd4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935741"
---
# <span data-ttu-id="db888-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="db888-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="db888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db888-102">SYNOPSIS</span></span>
<span data-ttu-id="db888-103">Günlük profili alır.</span><span class="sxs-lookup"><span data-stu-id="db888-103">Gets a log profile.</span></span>

## <span data-ttu-id="db888-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db888-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db888-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db888-105">DESCRIPTION</span></span>
<span data-ttu-id="db888-106">**Get-AzLogProfile** cmdlet 'i bir günlük profili alır.</span><span class="sxs-lookup"><span data-stu-id="db888-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="db888-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db888-107">EXAMPLES</span></span>

## <span data-ttu-id="db888-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db888-108">PARAMETERS</span></span>

### <span data-ttu-id="db888-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db888-109">-DefaultProfile</span></span>
<span data-ttu-id="db888-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="db888-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db888-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="db888-111">-Name</span></span>
<span data-ttu-id="db888-112">Alınacak günlük profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db888-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="db888-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db888-113">CommonParameters</span></span>
<span data-ttu-id="db888-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db888-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db888-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db888-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db888-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db888-116">INPUTS</span></span>

### <span data-ttu-id="db888-117">System. String</span><span class="sxs-lookup"><span data-stu-id="db888-117">System.String</span></span>

## <span data-ttu-id="db888-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db888-118">OUTPUTS</span></span>

### <span data-ttu-id="db888-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="db888-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="db888-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db888-120">NOTES</span></span>

## <span data-ttu-id="db888-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db888-121">RELATED LINKS</span></span>

[<span data-ttu-id="db888-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="db888-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="db888-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="db888-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


