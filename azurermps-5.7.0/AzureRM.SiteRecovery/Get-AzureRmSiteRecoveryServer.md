---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: feba4e66483aba9e77817aa2b473d0d22ae7d882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763979"
---
# <span data-ttu-id="6f8f4-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="6f8f4-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="6f8f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8f4-103">Geçerli kasaya kaydedilen site kurtarma sunucularıyla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="6f8f4-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f8f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f8f4-104">SYNTAX</span></span>

### <span data-ttu-id="6f8f4-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f8f4-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f8f4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f8f4-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f8f4-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6f8f4-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f8f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f8f4-108">DESCRIPTION</span></span>
<span data-ttu-id="6f8f4-109">**Get-AzureRmSiteRecoveryServer** cmdlet 'i, geçerli site kurtarma kasasına kaydedilen Azure Site Recovery sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6f8f4-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="6f8f4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f8f4-110">EXAMPLES</span></span>

## <span data-ttu-id="6f8f4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f8f4-111">PARAMETERS</span></span>

### <span data-ttu-id="6f8f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8f4-112">-DefaultProfile</span></span>
<span data-ttu-id="6f8f4-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f8f4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8f4-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6f8f4-114">-FriendlyName</span></span>
<span data-ttu-id="6f8f4-115">Sunucunun kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f8f4-115">Specifies the friendly name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8f4-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f8f4-116">-Name</span></span>
<span data-ttu-id="6f8f4-117">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f8f4-117">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f8f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8f4-118">CommonParameters</span></span>
<span data-ttu-id="6f8f4-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f8f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8f4-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8f4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8f4-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f8f4-121">INPUTS</span></span>

### <span data-ttu-id="6f8f4-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f8f4-122">None</span></span>
<span data-ttu-id="6f8f4-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6f8f4-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f8f4-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f8f4-124">OUTPUTS</span></span>

### <span data-ttu-id="6f8f4-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="6f8f4-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="6f8f4-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f8f4-126">NOTES</span></span>

## <span data-ttu-id="6f8f4-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f8f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="6f8f4-128">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="6f8f4-128">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
