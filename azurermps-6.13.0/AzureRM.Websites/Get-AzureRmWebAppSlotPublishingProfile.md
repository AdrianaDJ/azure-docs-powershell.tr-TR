---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572558"
---
# <span data-ttu-id="bc7be-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="bc7be-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="bc7be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc7be-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7be-103">Bir Azure Web App yuva yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="bc7be-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc7be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc7be-104">SYNTAX</span></span>

### <span data-ttu-id="bc7be-105">S1</span><span class="sxs-lookup"><span data-stu-id="bc7be-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7be-106">S2</span><span class="sxs-lookup"><span data-stu-id="bc7be-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc7be-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc7be-107">DESCRIPTION</span></span>
<span data-ttu-id="bc7be-108">**Get-AzureRmWebAppSlotPublishingProfile** cmdlet 'i belirtilen yuva Için Web uygulaması yayımlama profilini alır.</span><span class="sxs-lookup"><span data-stu-id="bc7be-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="bc7be-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc7be-109">EXAMPLES</span></span>

### <span data-ttu-id="bc7be-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc7be-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="bc7be-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilişkilendirilmiş yuva Slot001 için yayımlama profilini alır ve bu profili belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="bc7be-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="bc7be-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc7be-112">PARAMETERS</span></span>

### <span data-ttu-id="bc7be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7be-113">-DefaultProfile</span></span>
<span data-ttu-id="bc7be-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc7be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc7be-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="bc7be-115">-Format</span></span>
<span data-ttu-id="bc7be-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="bc7be-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7be-117">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="bc7be-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="bc7be-118">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="bc7be-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7be-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc7be-119">-Name</span></span>
<span data-ttu-id="bc7be-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="bc7be-120">WebApp Name</span></span>

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

### <span data-ttu-id="bc7be-121">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="bc7be-121">-OutputFile</span></span>
<span data-ttu-id="bc7be-122">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="bc7be-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc7be-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc7be-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bc7be-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bc7be-125">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="bc7be-125">-Slot</span></span>
<span data-ttu-id="bc7be-126">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="bc7be-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bc7be-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bc7be-127">-WebApp</span></span>
<span data-ttu-id="bc7be-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="bc7be-128">WebApp Object</span></span>

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

### <span data-ttu-id="bc7be-129">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="bc7be-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="bc7be-130">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="bc7be-130">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7be-131">CommonParameters</span></span>
<span data-ttu-id="bc7be-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc7be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7be-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc7be-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7be-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc7be-134">INPUTS</span></span>

### <span data-ttu-id="bc7be-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bc7be-135">System.String</span></span>

### <span data-ttu-id="bc7be-136">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="bc7be-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="bc7be-137">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc7be-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="bc7be-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc7be-138">OUTPUTS</span></span>

### <span data-ttu-id="bc7be-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bc7be-139">System.String</span></span>

## <span data-ttu-id="bc7be-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc7be-140">NOTES</span></span>

## <span data-ttu-id="bc7be-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc7be-141">RELATED LINKS</span></span>

[<span data-ttu-id="bc7be-142">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="bc7be-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="bc7be-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bc7be-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="bc7be-144">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bc7be-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
