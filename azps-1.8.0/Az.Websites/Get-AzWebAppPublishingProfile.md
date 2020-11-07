---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: a89ebd3142d738664cd80cab198bd6f791c1287a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753831"
---
# <span data-ttu-id="8f059-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="8f059-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="8f059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f059-102">SYNOPSIS</span></span>
<span data-ttu-id="8f059-103">Bir Azure Web App yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="8f059-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="8f059-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f059-104">SYNTAX</span></span>

### <span data-ttu-id="8f059-105">S1</span><span class="sxs-lookup"><span data-stu-id="8f059-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f059-106">S2</span><span class="sxs-lookup"><span data-stu-id="8f059-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f059-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f059-107">DESCRIPTION</span></span>
<span data-ttu-id="8f059-108">**Get-AzWebAppPublishingProfile** cmdlet 'ı bir Azure Web App Publishing profili alır.</span><span class="sxs-lookup"><span data-stu-id="8f059-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="8f059-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f059-109">EXAMPLES</span></span>

### <span data-ttu-id="8f059-110">2</span><span class="sxs-lookup"><span data-stu-id="8f059-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="8f059-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yayımlama profilini alır ve belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="8f059-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="8f059-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f059-112">PARAMETERS</span></span>

### <span data-ttu-id="8f059-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f059-113">-DefaultProfile</span></span>
<span data-ttu-id="8f059-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f059-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f059-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="8f059-115">-Format</span></span>
<span data-ttu-id="8f059-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="8f059-116">Format</span></span>

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

### <span data-ttu-id="8f059-117">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="8f059-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="8f059-118">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="8f059-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="8f059-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f059-119">-Name</span></span>
<span data-ttu-id="8f059-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8f059-120">WebApp Name</span></span>

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

### <span data-ttu-id="8f059-121">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="8f059-121">-OutputFile</span></span>
<span data-ttu-id="8f059-122">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="8f059-122">Output File</span></span>

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

### <span data-ttu-id="8f059-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f059-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f059-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8f059-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8f059-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8f059-125">-WebApp</span></span>
<span data-ttu-id="8f059-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8f059-126">WebApp Object</span></span>

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

### <span data-ttu-id="8f059-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f059-127">CommonParameters</span></span>
<span data-ttu-id="8f059-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f059-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f059-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f059-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f059-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f059-130">INPUTS</span></span>

### <span data-ttu-id="8f059-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8f059-131">System.String</span></span>

### <span data-ttu-id="8f059-132">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="8f059-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8f059-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f059-133">OUTPUTS</span></span>

### <span data-ttu-id="8f059-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8f059-134">System.String</span></span>

## <span data-ttu-id="8f059-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f059-135">NOTES</span></span>

## <span data-ttu-id="8f059-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f059-136">RELATED LINKS</span></span>

[<span data-ttu-id="8f059-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8f059-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="8f059-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8f059-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


