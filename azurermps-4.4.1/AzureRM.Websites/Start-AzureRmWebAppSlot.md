---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 687adf3cd7101a9747346c4b1aa3ba201d6dcc46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586861"
---
# <span data-ttu-id="a1b91-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b91-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a1b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b91-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b91-103">Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="a1b91-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1b91-104">SYNTAX</span></span>

### <span data-ttu-id="a1b91-105">S1</span><span class="sxs-lookup"><span data-stu-id="a1b91-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b91-106">S2</span><span class="sxs-lookup"><span data-stu-id="a1b91-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b91-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1b91-107">DESCRIPTION</span></span>
<span data-ttu-id="a1b91-108">**Start-AzureRmWebAppSlot** cmdlet 'ı Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="a1b91-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="a1b91-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1b91-109">EXAMPLES</span></span>

### <span data-ttu-id="a1b91-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a1b91-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="a1b91-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adındaki Web uygulamasının Slot001 adlı yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="a1b91-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a1b91-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1b91-112">PARAMETERS</span></span>

### <span data-ttu-id="a1b91-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1b91-113">-Name</span></span>
<span data-ttu-id="a1b91-114">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="a1b91-114">WebApp Name</span></span>

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

### <span data-ttu-id="a1b91-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b91-115">-ResourceGroupName</span></span>
<span data-ttu-id="a1b91-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a1b91-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a1b91-117">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a1b91-117">-Slot</span></span>
<span data-ttu-id="a1b91-118">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="a1b91-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a1b91-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a1b91-119">-WebApp</span></span>
<span data-ttu-id="a1b91-120">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="a1b91-120">WebApp Object</span></span>

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

### <span data-ttu-id="a1b91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b91-121">-DefaultProfile</span></span>
<span data-ttu-id="a1b91-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1b91-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b91-123">CommonParameters</span></span>
<span data-ttu-id="a1b91-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1b91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b91-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b91-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b91-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1b91-126">INPUTS</span></span>

### <span data-ttu-id="a1b91-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="a1b91-127">Site</span></span>
<span data-ttu-id="a1b91-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a1b91-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a1b91-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1b91-129">OUTPUTS</span></span>

## <span data-ttu-id="a1b91-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1b91-130">NOTES</span></span>

## <span data-ttu-id="a1b91-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1b91-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1b91-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b91-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1b91-133">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b91-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1b91-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b91-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1b91-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b91-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1b91-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b91-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1b91-137">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b91-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="a1b91-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a1b91-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
