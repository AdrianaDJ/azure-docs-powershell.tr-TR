---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936080"
---
# <span data-ttu-id="13644-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13644-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="13644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13644-102">SYNOPSIS</span></span>

## <span data-ttu-id="13644-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13644-103">SYNTAX</span></span>

### <span data-ttu-id="13644-104">S1</span><span class="sxs-lookup"><span data-stu-id="13644-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13644-105">S2</span><span class="sxs-lookup"><span data-stu-id="13644-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13644-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="13644-106">DESCRIPTION</span></span>
<span data-ttu-id="13644-107">**Remove-AzWebAppSlot** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web App yuvasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13644-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="13644-108">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13644-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="13644-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13644-109">EXAMPLES</span></span>

### <span data-ttu-id="13644-110">Örnek 1: Web uygulaması yuvasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="13644-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="13644-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait Web App Contosositesiyle ilişkili Slot001 adlı yuvayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="13644-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="13644-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13644-112">PARAMETERS</span></span>

### <span data-ttu-id="13644-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13644-113">-DefaultProfile</span></span>
<span data-ttu-id="13644-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13644-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13644-115">-Force</span><span class="sxs-lookup"><span data-stu-id="13644-115">-Force</span></span>
<span data-ttu-id="13644-116">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="13644-116">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13644-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="13644-117">-Name</span></span>
<span data-ttu-id="13644-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="13644-118">WebApp Name</span></span>

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

### <span data-ttu-id="13644-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13644-119">-ResourceGroupName</span></span>
<span data-ttu-id="13644-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="13644-120">Resource Group Name</span></span>

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

### <span data-ttu-id="13644-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="13644-121">-Slot</span></span>
<span data-ttu-id="13644-122">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="13644-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="13644-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="13644-123">-WebApp</span></span>
<span data-ttu-id="13644-124">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="13644-124">WebApp Object</span></span>

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

### <span data-ttu-id="13644-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="13644-125">-Confirm</span></span>
<span data-ttu-id="13644-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="13644-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13644-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13644-127">-WhatIf</span></span>
<span data-ttu-id="13644-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13644-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13644-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="13644-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="13644-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="13644-130">-AsJob</span></span>
<span data-ttu-id="13644-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="13644-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13644-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13644-132">CommonParameters</span></span>
<span data-ttu-id="13644-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13644-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13644-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13644-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13644-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13644-135">INPUTS</span></span>

### <span data-ttu-id="13644-136">Bölge</span><span class="sxs-lookup"><span data-stu-id="13644-136">Site</span></span>
<span data-ttu-id="13644-137">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="13644-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="13644-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13644-138">OUTPUTS</span></span>

### <span data-ttu-id="13644-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="13644-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="13644-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13644-140">NOTES</span></span>

## <span data-ttu-id="13644-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13644-141">RELATED LINKS</span></span>

[<span data-ttu-id="13644-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13644-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="13644-143">Yeni-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13644-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="13644-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13644-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="13644-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13644-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="13644-146">Başlangıç-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13644-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="13644-147">Dur-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13644-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="13644-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="13644-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
