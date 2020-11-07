---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936059"
---
# <span data-ttu-id="8d4b7-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d4b7-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="8d4b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4b7-103">Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="8d4b7-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="8d4b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d4b7-104">SYNTAX</span></span>

### <span data-ttu-id="8d4b7-105">S1</span><span class="sxs-lookup"><span data-stu-id="8d4b7-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d4b7-106">S2</span><span class="sxs-lookup"><span data-stu-id="8d4b7-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d4b7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d4b7-107">DESCRIPTION</span></span>
<span data-ttu-id="8d4b7-108">**Start-AzWebAppSlot** cmdlet 'ı Azure Web App yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="8d4b7-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="8d4b7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d4b7-109">EXAMPLES</span></span>

### <span data-ttu-id="8d4b7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8d4b7-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="8d4b7-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoWebApp adındaki Web uygulamasının Slot001 adlı yuvasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="8d4b7-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8d4b7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d4b7-112">PARAMETERS</span></span>

### <span data-ttu-id="8d4b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4b7-113">-DefaultProfile</span></span>
<span data-ttu-id="8d4b7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d4b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d4b7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d4b7-115">-Name</span></span>
<span data-ttu-id="8d4b7-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8d4b7-116">WebApp Name</span></span>

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

### <span data-ttu-id="8d4b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="8d4b7-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8d4b7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8d4b7-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="8d4b7-119">-Slot</span></span>
<span data-ttu-id="8d4b7-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="8d4b7-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8d4b7-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8d4b7-121">-WebApp</span></span>
<span data-ttu-id="8d4b7-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8d4b7-122">WebApp Object</span></span>

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

### <span data-ttu-id="8d4b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4b7-123">CommonParameters</span></span>
<span data-ttu-id="8d4b7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d4b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4b7-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d4b7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4b7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d4b7-126">INPUTS</span></span>

### <span data-ttu-id="8d4b7-127">Bölge</span><span class="sxs-lookup"><span data-stu-id="8d4b7-127">Site</span></span>
<span data-ttu-id="8d4b7-128">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8d4b7-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8d4b7-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d4b7-129">OUTPUTS</span></span>

## <span data-ttu-id="8d4b7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d4b7-130">NOTES</span></span>

## <span data-ttu-id="8d4b7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d4b7-131">RELATED LINKS</span></span>

[<span data-ttu-id="8d4b7-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d4b7-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8d4b7-133">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d4b7-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8d4b7-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d4b7-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8d4b7-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d4b7-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8d4b7-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d4b7-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8d4b7-137">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d4b7-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8d4b7-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8d4b7-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
