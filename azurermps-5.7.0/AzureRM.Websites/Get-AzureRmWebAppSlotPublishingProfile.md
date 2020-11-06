---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: dbbab46f0363273e53af93db94cb283866af70b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588678"
---
# <span data-ttu-id="1dbd4-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1dbd4-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="1dbd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbd4-103">Bir Azure Web App yuva yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="1dbd4-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dbd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dbd4-104">SYNTAX</span></span>

### <span data-ttu-id="1dbd4-105">S1</span><span class="sxs-lookup"><span data-stu-id="1dbd4-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dbd4-106">S2</span><span class="sxs-lookup"><span data-stu-id="1dbd4-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbd4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dbd4-107">DESCRIPTION</span></span>
<span data-ttu-id="1dbd4-108">**Get-AzureRmWebAppSlotPublishingProfile** cmdlet 'i belirtilen yuva Için Web uygulaması yayımlama profilini alır.</span><span class="sxs-lookup"><span data-stu-id="1dbd4-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="1dbd4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dbd4-109">EXAMPLES</span></span>

### <span data-ttu-id="1dbd4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1dbd4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="1dbd4-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp ile ilişkilendirilmiş yuva Slot001 için yayımlama profilini alır ve bu profili belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="1dbd4-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="1dbd4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dbd4-112">PARAMETERS</span></span>

### <span data-ttu-id="1dbd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbd4-113">-DefaultProfile</span></span>
<span data-ttu-id="1dbd4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dbd4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbd4-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="1dbd4-115">-Format</span></span>
<span data-ttu-id="1dbd4-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="1dbd4-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbd4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1dbd4-117">-Name</span></span>
<span data-ttu-id="1dbd4-118">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="1dbd4-118">WebApp Name</span></span>

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

### <span data-ttu-id="1dbd4-119">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="1dbd4-119">-OutputFile</span></span>
<span data-ttu-id="1dbd4-120">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="1dbd4-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbd4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbd4-121">-ResourceGroupName</span></span>
<span data-ttu-id="1dbd4-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1dbd4-122">Resource Group Name</span></span>

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

### <span data-ttu-id="1dbd4-123">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="1dbd4-123">-Slot</span></span>
<span data-ttu-id="1dbd4-124">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="1dbd4-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1dbd4-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1dbd4-125">-WebApp</span></span>
<span data-ttu-id="1dbd4-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="1dbd4-126">WebApp Object</span></span>

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

### <span data-ttu-id="1dbd4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbd4-127">CommonParameters</span></span>
<span data-ttu-id="1dbd4-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dbd4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbd4-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbd4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbd4-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dbd4-130">INPUTS</span></span>

### <span data-ttu-id="1dbd4-131">Bölge</span><span class="sxs-lookup"><span data-stu-id="1dbd4-131">Site</span></span>
<span data-ttu-id="1dbd4-132">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1dbd4-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1dbd4-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dbd4-133">OUTPUTS</span></span>

## <span data-ttu-id="1dbd4-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dbd4-134">NOTES</span></span>

## <span data-ttu-id="1dbd4-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dbd4-135">RELATED LINKS</span></span>

[<span data-ttu-id="1dbd4-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1dbd4-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="1dbd4-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1dbd4-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="1dbd4-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1dbd4-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
