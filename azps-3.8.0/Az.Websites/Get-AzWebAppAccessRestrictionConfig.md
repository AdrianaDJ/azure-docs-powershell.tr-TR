---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937602"
---
# <span data-ttu-id="4e21c-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4e21c-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="4e21c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e21c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e21c-103">Azure Web App için Access 'in birlikte yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="4e21c-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="4e21c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e21c-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e21c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e21c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e21c-106">**Get-AzWebAppAccessRestrictionConfig** cmdlet 'ı bir Azure Web uygulaması hakkında erişim kısıtlama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="4e21c-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="4e21c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e21c-107">EXAMPLES</span></span>

### <span data-ttu-id="4e21c-108">Örnek 1: kaynak grubundan Web uygulaması erişim kısıtlaması yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="4e21c-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="4e21c-109">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan ContosoSite adlı Web uygulamasının erişim kısıtlama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="4e21c-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4e21c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e21c-110">PARAMETERS</span></span>

### <span data-ttu-id="4e21c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e21c-111">-DefaultProfile</span></span>
<span data-ttu-id="4e21c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e21c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e21c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e21c-113">-Name</span></span>
<span data-ttu-id="4e21c-114">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="4e21c-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e21c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e21c-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e21c-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4e21c-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e21c-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="4e21c-117">-SlotName</span></span>
<span data-ttu-id="4e21c-118">Dağıtım yuvası adı.</span><span class="sxs-lookup"><span data-stu-id="4e21c-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e21c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e21c-119">CommonParameters</span></span>
<span data-ttu-id="4e21c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e21c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e21c-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4e21c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e21c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e21c-122">INPUTS</span></span>

### <span data-ttu-id="4e21c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4e21c-123">System.String</span></span>

## <span data-ttu-id="4e21c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e21c-124">OUTPUTS</span></span>

### <span data-ttu-id="4e21c-125">Microsoft. Azure. Commands. WebApps. modeller. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4e21c-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="4e21c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e21c-126">NOTES</span></span>

## <span data-ttu-id="4e21c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e21c-127">RELATED LINKS</span></span>

[<span data-ttu-id="4e21c-128">Güncelleştirme-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4e21c-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="4e21c-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4e21c-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="4e21c-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4e21c-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
