---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936065"
---
# <span data-ttu-id="d498e-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d498e-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="d498e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d498e-102">SYNOPSIS</span></span>

## <span data-ttu-id="d498e-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d498e-103">SYNTAX</span></span>

### <span data-ttu-id="d498e-104">S1</span><span class="sxs-lookup"><span data-stu-id="d498e-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d498e-105">S2</span><span class="sxs-lookup"><span data-stu-id="d498e-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d498e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d498e-106">DESCRIPTION</span></span>
<span data-ttu-id="d498e-107">**Restart-AzWebAppSlot** cmdlet 'i durur ve bir Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="d498e-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="d498e-108">Web uygulaması yuvası durdurulmuş durumdaysa, Start-AzWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d498e-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="d498e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d498e-109">EXAMPLES</span></span>

### <span data-ttu-id="d498e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d498e-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d498e-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yuva Slot001</span><span class="sxs-lookup"><span data-stu-id="d498e-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d498e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d498e-112">PARAMETERS</span></span>

### <span data-ttu-id="d498e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d498e-113">-DefaultProfile</span></span>
<span data-ttu-id="d498e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d498e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d498e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d498e-115">-Name</span></span>
<span data-ttu-id="d498e-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d498e-116">WebApp Name</span></span>

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

### <span data-ttu-id="d498e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d498e-117">-ResourceGroupName</span></span>
<span data-ttu-id="d498e-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d498e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d498e-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d498e-119">-Slot</span></span>
<span data-ttu-id="d498e-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="d498e-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d498e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d498e-121">-WebApp</span></span>
<span data-ttu-id="d498e-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="d498e-122">WebApp Object</span></span>

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

### <span data-ttu-id="d498e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d498e-123">CommonParameters</span></span>
<span data-ttu-id="d498e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d498e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d498e-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d498e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d498e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d498e-126">INPUTS</span></span>

### <span data-ttu-id="d498e-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="d498e-127">Site</span></span>
<span data-ttu-id="d498e-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d498e-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d498e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d498e-129">OUTPUTS</span></span>

## <span data-ttu-id="d498e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d498e-130">NOTES</span></span>

## <span data-ttu-id="d498e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d498e-131">RELATED LINKS</span></span>

[<span data-ttu-id="d498e-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d498e-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d498e-133">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d498e-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d498e-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d498e-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d498e-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d498e-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="d498e-136">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d498e-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d498e-137">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d498e-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d498e-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d498e-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
