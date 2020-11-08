---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098391"
---
# <span data-ttu-id="f466b-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f466b-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="f466b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f466b-102">SYNOPSIS</span></span>

## <span data-ttu-id="f466b-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f466b-103">SYNTAX</span></span>

### <span data-ttu-id="f466b-104">S1</span><span class="sxs-lookup"><span data-stu-id="f466b-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f466b-105">S2</span><span class="sxs-lookup"><span data-stu-id="f466b-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f466b-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="f466b-106">DESCRIPTION</span></span>
<span data-ttu-id="f466b-107">**Restart-AzWebAppSlot** cmdlet 'i durur ve bir Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="f466b-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="f466b-108">Web uygulaması yuvası durdurulmuş durumdaysa, Start-AzWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f466b-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="f466b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f466b-109">EXAMPLES</span></span>

### <span data-ttu-id="f466b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f466b-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="f466b-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yuva Slot001</span><span class="sxs-lookup"><span data-stu-id="f466b-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="f466b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f466b-112">PARAMETERS</span></span>

### <span data-ttu-id="f466b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f466b-113">-DefaultProfile</span></span>
<span data-ttu-id="f466b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f466b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f466b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f466b-115">-Name</span></span>
<span data-ttu-id="f466b-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="f466b-116">WebApp Name</span></span>

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

### <span data-ttu-id="f466b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f466b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f466b-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f466b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f466b-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="f466b-119">-Slot</span></span>
<span data-ttu-id="f466b-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="f466b-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f466b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f466b-121">-WebApp</span></span>
<span data-ttu-id="f466b-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="f466b-122">WebApp Object</span></span>

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

### <span data-ttu-id="f466b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f466b-123">CommonParameters</span></span>
<span data-ttu-id="f466b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f466b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f466b-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f466b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f466b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f466b-126">INPUTS</span></span>

### <span data-ttu-id="f466b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f466b-127">System.String</span></span>

### <span data-ttu-id="f466b-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="f466b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f466b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f466b-129">OUTPUTS</span></span>

### <span data-ttu-id="f466b-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="f466b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f466b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f466b-131">NOTES</span></span>

## <span data-ttu-id="f466b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f466b-132">RELATED LINKS</span></span>

[<span data-ttu-id="f466b-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f466b-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f466b-134">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f466b-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="f466b-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f466b-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="f466b-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f466b-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="f466b-137">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f466b-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="f466b-138">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f466b-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f466b-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f466b-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
