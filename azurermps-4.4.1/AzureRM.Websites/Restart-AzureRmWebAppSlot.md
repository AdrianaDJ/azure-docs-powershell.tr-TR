---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: ace1b16bc6d89fb619daba23a214326acd8d0d24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586866"
---
# <span data-ttu-id="5f691-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f691-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="5f691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f691-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f691-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f691-103">SYNTAX</span></span>

### <span data-ttu-id="5f691-104">S1</span><span class="sxs-lookup"><span data-stu-id="5f691-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f691-105">S2</span><span class="sxs-lookup"><span data-stu-id="5f691-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f691-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f691-106">DESCRIPTION</span></span>
<span data-ttu-id="5f691-107">**Restart-AzureRmWebAppSlot** cmdlet 'i durur ve bir Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="5f691-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="5f691-108">Web uygulaması yuvası durdurulmuş durumdaysa, Start-AzureRmWebAppSlot cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5f691-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="5f691-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f691-109">EXAMPLES</span></span>

### <span data-ttu-id="5f691-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f691-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="5f691-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yuva Slot001</span><span class="sxs-lookup"><span data-stu-id="5f691-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5f691-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f691-112">PARAMETERS</span></span>

### <span data-ttu-id="5f691-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f691-113">-Name</span></span>
<span data-ttu-id="5f691-114">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="5f691-114">WebApp Name</span></span>

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

### <span data-ttu-id="5f691-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f691-115">-ResourceGroupName</span></span>
<span data-ttu-id="5f691-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5f691-116">Resource Group Name</span></span>

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

### <span data-ttu-id="5f691-117">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="5f691-117">-Slot</span></span>
<span data-ttu-id="5f691-118">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="5f691-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5f691-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5f691-119">-WebApp</span></span>
<span data-ttu-id="5f691-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="5f691-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f691-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f691-121">-DefaultProfile</span></span>
<span data-ttu-id="5f691-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f691-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f691-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f691-123">CommonParameters</span></span>
<span data-ttu-id="5f691-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f691-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f691-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f691-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f691-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f691-126">INPUTS</span></span>

### <span data-ttu-id="5f691-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="5f691-127">Site</span></span>
<span data-ttu-id="5f691-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5f691-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5f691-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f691-129">OUTPUTS</span></span>

## <span data-ttu-id="5f691-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f691-130">NOTES</span></span>

## <span data-ttu-id="5f691-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f691-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f691-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f691-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="5f691-133">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f691-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="5f691-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f691-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="5f691-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f691-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="5f691-136">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f691-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="5f691-137">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5f691-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="5f691-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f691-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
