---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: ad3ff3dbd5589a890ecf7649c9a9b66843b8b444
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939975"
---
# <span data-ttu-id="4e389-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4e389-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="4e389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e389-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e389-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e389-103">SYNTAX</span></span>

### <span data-ttu-id="4e389-104">S1</span><span class="sxs-lookup"><span data-stu-id="4e389-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e389-105">S2</span><span class="sxs-lookup"><span data-stu-id="4e389-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e389-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e389-106">DESCRIPTION</span></span>
<span data-ttu-id="4e389-107">**Restart-AzureRmWebAppSlot** cmdlet 'i durur ve bir Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="4e389-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="4e389-108">Web uygulaması yuvası durdurulmuş durumdaysa, Start-AzureRmWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e389-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="4e389-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e389-109">EXAMPLES</span></span>

### <span data-ttu-id="4e389-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4e389-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="4e389-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yuva Slot001</span><span class="sxs-lookup"><span data-stu-id="4e389-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4e389-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e389-112">PARAMETERS</span></span>

### <span data-ttu-id="4e389-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e389-113">-DefaultProfile</span></span>
<span data-ttu-id="4e389-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e389-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e389-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e389-115">-Name</span></span>
<span data-ttu-id="4e389-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="4e389-116">WebApp Name</span></span>

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

### <span data-ttu-id="4e389-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e389-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e389-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4e389-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4e389-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4e389-119">-Slot</span></span>
<span data-ttu-id="4e389-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="4e389-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e389-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4e389-121">-WebApp</span></span>
<span data-ttu-id="4e389-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="4e389-122">WebApp Object</span></span>

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

### <span data-ttu-id="4e389-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e389-123">CommonParameters</span></span>
<span data-ttu-id="4e389-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e389-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e389-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e389-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e389-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e389-126">INPUTS</span></span>

### <span data-ttu-id="4e389-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="4e389-127">Site</span></span>
<span data-ttu-id="4e389-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4e389-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4e389-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e389-129">OUTPUTS</span></span>

## <span data-ttu-id="4e389-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e389-130">NOTES</span></span>

## <span data-ttu-id="4e389-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e389-131">RELATED LINKS</span></span>

[<span data-ttu-id="4e389-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4e389-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="4e389-133">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4e389-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="4e389-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4e389-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="4e389-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4e389-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="4e389-136">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4e389-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="4e389-137">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4e389-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="4e389-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4e389-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
