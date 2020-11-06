---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594529"
---
# <span data-ttu-id="80d25-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d25-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="80d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d25-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80d25-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80d25-103">SYNTAX</span></span>

### <span data-ttu-id="80d25-104">S1</span><span class="sxs-lookup"><span data-stu-id="80d25-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d25-105">S2</span><span class="sxs-lookup"><span data-stu-id="80d25-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d25-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="80d25-106">DESCRIPTION</span></span>
<span data-ttu-id="80d25-107">**Remove-AzureRmWebAppSlot** cmdlet 'i, kaynak grubuna ve Web uygulaması adına sağlanan bir Azure Web App yuvasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80d25-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="80d25-108">Bu cmdlet varsayılan olarak tüm yuvaları ve ölçümleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80d25-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="80d25-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80d25-109">EXAMPLES</span></span>

### <span data-ttu-id="80d25-110">Örnek 1: Web uygulaması yuvasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="80d25-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="80d25-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait Web App Contosositesiyle ilişkili Slot001 adlı yuvayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80d25-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="80d25-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80d25-112">PARAMETERS</span></span>

### <span data-ttu-id="80d25-113">-Force</span><span class="sxs-lookup"><span data-stu-id="80d25-113">-Force</span></span>
<span data-ttu-id="80d25-114">Zorla Kaldır seçeneği</span><span class="sxs-lookup"><span data-stu-id="80d25-114">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d25-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="80d25-115">-Name</span></span>
<span data-ttu-id="80d25-116">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="80d25-116">WebApp Name</span></span>

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

### <span data-ttu-id="80d25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d25-117">-ResourceGroupName</span></span>
<span data-ttu-id="80d25-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="80d25-118">Resource Group Name</span></span>

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

### <span data-ttu-id="80d25-119">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="80d25-119">-Slot</span></span>
<span data-ttu-id="80d25-120">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="80d25-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="80d25-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="80d25-121">-WebApp</span></span>
<span data-ttu-id="80d25-122">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="80d25-122">WebApp Object</span></span>

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

### <span data-ttu-id="80d25-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="80d25-123">-Confirm</span></span>
<span data-ttu-id="80d25-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="80d25-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d25-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d25-125">-WhatIf</span></span>
<span data-ttu-id="80d25-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="80d25-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d25-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="80d25-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d25-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d25-128">-DefaultProfile</span></span>
<span data-ttu-id="80d25-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80d25-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80d25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d25-130">CommonParameters</span></span>
<span data-ttu-id="80d25-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80d25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d25-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80d25-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d25-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80d25-133">INPUTS</span></span>

### <span data-ttu-id="80d25-134">Bölge</span><span class="sxs-lookup"><span data-stu-id="80d25-134">Site</span></span>
<span data-ttu-id="80d25-135">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="80d25-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="80d25-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80d25-136">OUTPUTS</span></span>

### <span data-ttu-id="80d25-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="80d25-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="80d25-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80d25-138">NOTES</span></span>

## <span data-ttu-id="80d25-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80d25-139">RELATED LINKS</span></span>

[<span data-ttu-id="80d25-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d25-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="80d25-141">Yeni-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d25-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="80d25-142">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d25-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="80d25-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d25-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="80d25-144">Başlangıç-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d25-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="80d25-145">Dur-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="80d25-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="80d25-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="80d25-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
