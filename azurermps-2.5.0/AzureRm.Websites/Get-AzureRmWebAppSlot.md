---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9ac20046317fa7d070e69284696293e1f66ed486
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939024"
---
# <span data-ttu-id="a9ced-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9ced-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a9ced-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ced-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ced-103">Bir Azure Web App yuvası alır.</span><span class="sxs-lookup"><span data-stu-id="a9ced-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9ced-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9ced-104">SYNTAX</span></span>

### <span data-ttu-id="a9ced-105">S1</span><span class="sxs-lookup"><span data-stu-id="a9ced-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ced-106">S2</span><span class="sxs-lookup"><span data-stu-id="a9ced-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9ced-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9ced-107">DESCRIPTION</span></span>
<span data-ttu-id="a9ced-108">**Get-AzureRmWebAppSlot** cmdlet 'ı Azure Web App yuvası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a9ced-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="a9ced-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9ced-109">EXAMPLES</span></span>

### <span data-ttu-id="a9ced-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9ced-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="a9ced-111">Bu komut, Default-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından Slot001 adlı yuvayı alır.</span><span class="sxs-lookup"><span data-stu-id="a9ced-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a9ced-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9ced-112">PARAMETERS</span></span>

### <span data-ttu-id="a9ced-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ced-113">-DefaultProfile</span></span>
<span data-ttu-id="a9ced-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9ced-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9ced-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9ced-115">-Name</span></span>
<span data-ttu-id="a9ced-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="a9ced-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ced-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ced-117">-ResourceGroupName</span></span>
<span data-ttu-id="a9ced-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a9ced-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ced-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a9ced-119">-Slot</span></span>
<span data-ttu-id="a9ced-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="a9ced-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ced-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a9ced-121">-WebApp</span></span>
<span data-ttu-id="a9ced-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="a9ced-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ced-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ced-123">CommonParameters</span></span>
<span data-ttu-id="a9ced-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9ced-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ced-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ced-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ced-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9ced-126">INPUTS</span></span>

### <span data-ttu-id="a9ced-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="a9ced-127">Site</span></span>
<span data-ttu-id="a9ced-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a9ced-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a9ced-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9ced-129">OUTPUTS</span></span>

## <span data-ttu-id="a9ced-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9ced-130">NOTES</span></span>

## <span data-ttu-id="a9ced-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9ced-131">RELATED LINKS</span></span>

[<span data-ttu-id="a9ced-132">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9ced-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="a9ced-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9ced-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="a9ced-134">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9ced-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="a9ced-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9ced-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="a9ced-136">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9ced-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="a9ced-137">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9ced-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="a9ced-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a9ced-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
