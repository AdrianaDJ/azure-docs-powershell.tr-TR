---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 97bf4078ca09ce250fea0d7c660629fbab651974
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939651"
---
# <span data-ttu-id="b3f50-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3f50-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="b3f50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3f50-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f50-103">Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="b3f50-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3f50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3f50-104">SYNTAX</span></span>

### <span data-ttu-id="b3f50-105">S1</span><span class="sxs-lookup"><span data-stu-id="b3f50-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f50-106">S2</span><span class="sxs-lookup"><span data-stu-id="b3f50-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3f50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3f50-107">DESCRIPTION</span></span>
<span data-ttu-id="b3f50-108">**Start-AzureRmWebAppSlot** cmdlet 'ı Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="b3f50-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="b3f50-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3f50-109">EXAMPLES</span></span>

### <span data-ttu-id="b3f50-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b3f50-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b3f50-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adındaki Web uygulamasının Slot001 adlı yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="b3f50-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b3f50-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3f50-112">PARAMETERS</span></span>

### <span data-ttu-id="b3f50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f50-113">-DefaultProfile</span></span>
<span data-ttu-id="b3f50-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3f50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3f50-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3f50-115">-Name</span></span>
<span data-ttu-id="b3f50-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="b3f50-116">WebApp Name</span></span>

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

### <span data-ttu-id="b3f50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f50-117">-ResourceGroupName</span></span>
<span data-ttu-id="b3f50-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b3f50-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b3f50-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="b3f50-119">-Slot</span></span>
<span data-ttu-id="b3f50-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="b3f50-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b3f50-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b3f50-121">-WebApp</span></span>
<span data-ttu-id="b3f50-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="b3f50-122">WebApp Object</span></span>

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

### <span data-ttu-id="b3f50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f50-123">CommonParameters</span></span>
<span data-ttu-id="b3f50-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3f50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f50-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3f50-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f50-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3f50-126">INPUTS</span></span>

### <span data-ttu-id="b3f50-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="b3f50-127">Site</span></span>
<span data-ttu-id="b3f50-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b3f50-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b3f50-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3f50-129">OUTPUTS</span></span>

## <span data-ttu-id="b3f50-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3f50-130">NOTES</span></span>

## <span data-ttu-id="b3f50-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3f50-131">RELATED LINKS</span></span>

[<span data-ttu-id="b3f50-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3f50-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b3f50-133">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3f50-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="b3f50-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3f50-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="b3f50-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3f50-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="b3f50-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3f50-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="b3f50-137">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b3f50-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="b3f50-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b3f50-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
