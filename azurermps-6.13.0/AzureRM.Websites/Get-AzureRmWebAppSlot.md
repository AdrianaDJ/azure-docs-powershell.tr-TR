---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572561"
---
# <span data-ttu-id="26671-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26671-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="26671-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26671-102">SYNOPSIS</span></span>
<span data-ttu-id="26671-103">Bir Azure Web App yuvası alır.</span><span class="sxs-lookup"><span data-stu-id="26671-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26671-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26671-104">SYNTAX</span></span>

### <span data-ttu-id="26671-105">S1</span><span class="sxs-lookup"><span data-stu-id="26671-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26671-106">S2</span><span class="sxs-lookup"><span data-stu-id="26671-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26671-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="26671-107">DESCRIPTION</span></span>
<span data-ttu-id="26671-108">**Get-AzureRmWebAppSlot** cmdlet 'ı Azure Web App yuvası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="26671-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="26671-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26671-109">EXAMPLES</span></span>

### <span data-ttu-id="26671-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26671-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="26671-111">Bu komut, Default-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından Slot001 adlı yuvayı alır.</span><span class="sxs-lookup"><span data-stu-id="26671-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="26671-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26671-112">PARAMETERS</span></span>

### <span data-ttu-id="26671-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26671-113">-DefaultProfile</span></span>
<span data-ttu-id="26671-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26671-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26671-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="26671-115">-Name</span></span>
<span data-ttu-id="26671-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="26671-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26671-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26671-117">-ResourceGroupName</span></span>
<span data-ttu-id="26671-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="26671-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26671-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="26671-119">-Slot</span></span>
<span data-ttu-id="26671-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="26671-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="26671-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="26671-121">-WebApp</span></span>
<span data-ttu-id="26671-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="26671-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26671-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26671-123">CommonParameters</span></span>
<span data-ttu-id="26671-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26671-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26671-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26671-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26671-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26671-126">INPUTS</span></span>

### <span data-ttu-id="26671-127">System. String</span><span class="sxs-lookup"><span data-stu-id="26671-127">System.String</span></span>

### <span data-ttu-id="26671-128">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="26671-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="26671-129">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26671-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="26671-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26671-130">OUTPUTS</span></span>

### <span data-ttu-id="26671-131">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="26671-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="26671-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26671-132">NOTES</span></span>

## <span data-ttu-id="26671-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26671-133">RELATED LINKS</span></span>

[<span data-ttu-id="26671-134">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26671-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="26671-135">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26671-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="26671-136">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26671-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="26671-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26671-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="26671-138">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26671-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="26671-139">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26671-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="26671-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="26671-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
