---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: a345b69fdc6695706f61a85c2926392c9f522aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587665"
---
# <span data-ttu-id="f5443-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5443-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="f5443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5443-102">SYNOPSIS</span></span>
<span data-ttu-id="f5443-103">CDN profili alır.</span><span class="sxs-lookup"><span data-stu-id="f5443-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5443-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5443-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5443-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5443-105">DESCRIPTION</span></span>
<span data-ttu-id="f5443-106">**Get-AzureRMCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profili ve ilgili bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="f5443-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="f5443-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5443-107">EXAMPLES</span></span>

## <span data-ttu-id="f5443-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5443-108">PARAMETERS</span></span>

### <span data-ttu-id="f5443-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5443-109">-DefaultProfile</span></span>
<span data-ttu-id="f5443-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f5443-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5443-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f5443-111">-ProfileName</span></span>
<span data-ttu-id="f5443-112">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5443-112">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5443-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5443-113">-ResourceGroupName</span></span>
<span data-ttu-id="f5443-114">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5443-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5443-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5443-115">CommonParameters</span></span>
<span data-ttu-id="f5443-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5443-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5443-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5443-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5443-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5443-118">INPUTS</span></span>

### <span data-ttu-id="f5443-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f5443-119">None</span></span>
<span data-ttu-id="f5443-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f5443-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5443-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5443-121">OUTPUTS</span></span>

###  
<span data-ttu-id="f5443-122">Bu cmdlet bir profil nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f5443-122">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="f5443-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5443-123">NOTES</span></span>

## <span data-ttu-id="f5443-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5443-124">RELATED LINKS</span></span>

[<span data-ttu-id="f5443-125">Yeni-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5443-125">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="f5443-126">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5443-126">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="f5443-127">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5443-127">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


