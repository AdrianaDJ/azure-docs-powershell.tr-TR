---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097324"
---
# <span data-ttu-id="cb146-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="cb146-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="cb146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb146-102">SYNOPSIS</span></span>
<span data-ttu-id="cb146-103">Bir Azure Web App yuva yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="cb146-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="cb146-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb146-104">SYNTAX</span></span>

### <span data-ttu-id="cb146-105">S1</span><span class="sxs-lookup"><span data-stu-id="cb146-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb146-106">S2</span><span class="sxs-lookup"><span data-stu-id="cb146-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb146-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb146-107">DESCRIPTION</span></span>
<span data-ttu-id="cb146-108">**Get-AzWebAppSlotPublishingProfile** cmdlet 'i, belirtilen yuva Için Web uygulaması yayımlama profilini alır.</span><span class="sxs-lookup"><span data-stu-id="cb146-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="cb146-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb146-109">EXAMPLES</span></span>

### <span data-ttu-id="cb146-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb146-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="cb146-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilişkilendirilmiş yuva Slot001 için yayımlama profilini alır ve bu profili belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="cb146-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="cb146-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb146-112">PARAMETERS</span></span>

### <span data-ttu-id="cb146-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb146-113">-DefaultProfile</span></span>
<span data-ttu-id="cb146-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb146-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb146-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="cb146-115">-Format</span></span>
<span data-ttu-id="cb146-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="cb146-116">Format</span></span>

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

### <span data-ttu-id="cb146-117">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="cb146-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="cb146-118">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="cb146-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="cb146-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb146-119">-Name</span></span>
<span data-ttu-id="cb146-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="cb146-120">WebApp Name</span></span>

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

### <span data-ttu-id="cb146-121">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="cb146-121">-OutputFile</span></span>
<span data-ttu-id="cb146-122">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="cb146-122">Output File</span></span>

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

### <span data-ttu-id="cb146-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb146-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb146-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cb146-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cb146-125">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="cb146-125">-Slot</span></span>
<span data-ttu-id="cb146-126">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="cb146-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="cb146-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cb146-127">-WebApp</span></span>
<span data-ttu-id="cb146-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="cb146-128">WebApp Object</span></span>

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

### <span data-ttu-id="cb146-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb146-129">CommonParameters</span></span>
<span data-ttu-id="cb146-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb146-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb146-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb146-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb146-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb146-132">INPUTS</span></span>

### <span data-ttu-id="cb146-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cb146-133">System.String</span></span>

### <span data-ttu-id="cb146-134">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="cb146-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cb146-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb146-135">OUTPUTS</span></span>

### <span data-ttu-id="cb146-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb146-136">System.String</span></span>

## <span data-ttu-id="cb146-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb146-137">NOTES</span></span>

## <span data-ttu-id="cb146-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb146-138">RELATED LINKS</span></span>

[<span data-ttu-id="cb146-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="cb146-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="cb146-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cb146-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="cb146-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cb146-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
