---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589272"
---
# <span data-ttu-id="860a3-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="860a3-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="860a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="860a3-102">SYNOPSIS</span></span>
<span data-ttu-id="860a3-103">Bir Azure Web App yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="860a3-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="860a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="860a3-104">SYNTAX</span></span>

### <span data-ttu-id="860a3-105">S1</span><span class="sxs-lookup"><span data-stu-id="860a3-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="860a3-106">S2</span><span class="sxs-lookup"><span data-stu-id="860a3-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="860a3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="860a3-107">DESCRIPTION</span></span>
<span data-ttu-id="860a3-108">**Get-AzureRmWebAppPublishingProfile** cmdlet 'ı bir Azure Web App Publishing profili alır.</span><span class="sxs-lookup"><span data-stu-id="860a3-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="860a3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="860a3-109">EXAMPLES</span></span>

### <span data-ttu-id="860a3-110">2</span><span class="sxs-lookup"><span data-stu-id="860a3-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="860a3-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yayımlama profilini alır ve belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="860a3-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="860a3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="860a3-112">PARAMETERS</span></span>

### <span data-ttu-id="860a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860a3-113">-DefaultProfile</span></span>
<span data-ttu-id="860a3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="860a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860a3-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="860a3-115">-Format</span></span>
<span data-ttu-id="860a3-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="860a3-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860a3-117">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="860a3-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="860a3-118">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="860a3-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="860a3-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="860a3-119">-Name</span></span>
<span data-ttu-id="860a3-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="860a3-120">WebApp Name</span></span>

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

### <span data-ttu-id="860a3-121">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="860a3-121">-OutputFile</span></span>
<span data-ttu-id="860a3-122">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="860a3-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860a3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860a3-123">-ResourceGroupName</span></span>
<span data-ttu-id="860a3-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="860a3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="860a3-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="860a3-125">-WebApp</span></span>
<span data-ttu-id="860a3-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="860a3-126">WebApp Object</span></span>

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

### <span data-ttu-id="860a3-127">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="860a3-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="860a3-128">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="860a3-128">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="860a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860a3-129">CommonParameters</span></span>
<span data-ttu-id="860a3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="860a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860a3-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860a3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860a3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="860a3-132">INPUTS</span></span>

### <span data-ttu-id="860a3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="860a3-133">System.String</span></span>

### <span data-ttu-id="860a3-134">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="860a3-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="860a3-135">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="860a3-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="860a3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="860a3-136">OUTPUTS</span></span>

### <span data-ttu-id="860a3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="860a3-137">System.String</span></span>

## <span data-ttu-id="860a3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="860a3-138">NOTES</span></span>

## <span data-ttu-id="860a3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="860a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="860a3-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="860a3-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="860a3-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="860a3-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


