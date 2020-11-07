---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 615fcc228be9ef0e3e0d23c6463859c20ff7da11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917879"
---
# <span data-ttu-id="1dbdb-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1dbdb-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="1dbdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbdb-103">Bir Azure Web App yuva yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="1dbdb-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="1dbdb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dbdb-104">SYNTAX</span></span>

### <span data-ttu-id="1dbdb-105">S1</span><span class="sxs-lookup"><span data-stu-id="1dbdb-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbdb-106">S2</span><span class="sxs-lookup"><span data-stu-id="1dbdb-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbdb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dbdb-107">DESCRIPTION</span></span>
<span data-ttu-id="1dbdb-108">**Get-AzWebAppSlotPublishingProfile** cmdlet 'i, belirtilen yuva Için Web uygulaması yayımlama profilini alır.</span><span class="sxs-lookup"><span data-stu-id="1dbdb-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="1dbdb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dbdb-109">EXAMPLES</span></span>

### <span data-ttu-id="1dbdb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1dbdb-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="1dbdb-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilişkilendirilmiş yuva Slot001 için yayımlama profilini alır ve bu profili belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="1dbdb-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="1dbdb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dbdb-112">PARAMETERS</span></span>

### <span data-ttu-id="1dbdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbdb-113">-DefaultProfile</span></span>
<span data-ttu-id="1dbdb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dbdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dbdb-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="1dbdb-115">-Format</span></span>
<span data-ttu-id="1dbdb-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="1dbdb-116">Format</span></span>

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

### <span data-ttu-id="1dbdb-117">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="1dbdb-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="1dbdb-118">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="1dbdb-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="1dbdb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dbdb-119">-Name</span></span>
<span data-ttu-id="1dbdb-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="1dbdb-120">WebApp Name</span></span>

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

### <span data-ttu-id="1dbdb-121">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="1dbdb-121">-OutputFile</span></span>
<span data-ttu-id="1dbdb-122">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="1dbdb-122">Output File</span></span>

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

### <span data-ttu-id="1dbdb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbdb-123">-ResourceGroupName</span></span>
<span data-ttu-id="1dbdb-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1dbdb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1dbdb-125">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="1dbdb-125">-Slot</span></span>
<span data-ttu-id="1dbdb-126">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="1dbdb-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1dbdb-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1dbdb-127">-WebApp</span></span>
<span data-ttu-id="1dbdb-128">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="1dbdb-128">WebApp Object</span></span>

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

### <span data-ttu-id="1dbdb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbdb-129">CommonParameters</span></span>
<span data-ttu-id="1dbdb-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dbdb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbdb-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbdb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbdb-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dbdb-132">INPUTS</span></span>

### <span data-ttu-id="1dbdb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1dbdb-133">System.String</span></span>

### <span data-ttu-id="1dbdb-134">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="1dbdb-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1dbdb-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dbdb-135">OUTPUTS</span></span>

### <span data-ttu-id="1dbdb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1dbdb-136">System.String</span></span>

## <span data-ttu-id="1dbdb-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dbdb-137">NOTES</span></span>

## <span data-ttu-id="1dbdb-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dbdb-138">RELATED LINKS</span></span>

[<span data-ttu-id="1dbdb-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1dbdb-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="1dbdb-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1dbdb-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1dbdb-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1dbdb-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
