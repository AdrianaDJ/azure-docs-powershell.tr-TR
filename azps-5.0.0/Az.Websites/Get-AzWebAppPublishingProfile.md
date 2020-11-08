---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279421"
---
# <span data-ttu-id="af4b9-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="af4b9-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="af4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="af4b9-103">Bir Azure Web App yayımlama profili alır.</span><span class="sxs-lookup"><span data-stu-id="af4b9-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="af4b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af4b9-104">SYNTAX</span></span>

### <span data-ttu-id="af4b9-105">S1</span><span class="sxs-lookup"><span data-stu-id="af4b9-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af4b9-106">S2</span><span class="sxs-lookup"><span data-stu-id="af4b9-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af4b9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af4b9-107">DESCRIPTION</span></span>
<span data-ttu-id="af4b9-108">**Get-AzWebAppPublishingProfile** cmdlet 'ı bir Azure Web App Publishing profili alır.</span><span class="sxs-lookup"><span data-stu-id="af4b9-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="af4b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af4b9-109">EXAMPLES</span></span>

### <span data-ttu-id="af4b9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af4b9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="af4b9-111">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp için yayımlama profilini alır ve belirtilen çıkış dosyasında depolar.</span><span class="sxs-lookup"><span data-stu-id="af4b9-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="af4b9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af4b9-112">PARAMETERS</span></span>

### <span data-ttu-id="af4b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4b9-113">-DefaultProfile</span></span>
<span data-ttu-id="af4b9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af4b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af4b9-115">Biçimli</span><span class="sxs-lookup"><span data-stu-id="af4b9-115">-Format</span></span>
<span data-ttu-id="af4b9-116">Formatlamak</span><span class="sxs-lookup"><span data-stu-id="af4b9-116">Format</span></span>

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

### <span data-ttu-id="af4b9-117">-Includedeyıldız</span><span class="sxs-lookup"><span data-stu-id="af4b9-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="af4b9-118">Doğru olduğunda olağanüstü durum kurtarma uç noktalarını Ekle</span><span class="sxs-lookup"><span data-stu-id="af4b9-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="af4b9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="af4b9-119">-Name</span></span>
<span data-ttu-id="af4b9-120">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="af4b9-120">WebApp Name</span></span>

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

### <span data-ttu-id="af4b9-121">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="af4b9-121">-OutputFile</span></span>
<span data-ttu-id="af4b9-122">Çıkış dosyası</span><span class="sxs-lookup"><span data-stu-id="af4b9-122">Output File</span></span>

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

### <span data-ttu-id="af4b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="af4b9-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="af4b9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="af4b9-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="af4b9-125">-WebApp</span></span>
<span data-ttu-id="af4b9-126">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="af4b9-126">WebApp Object</span></span>

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

### <span data-ttu-id="af4b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4b9-127">CommonParameters</span></span>
<span data-ttu-id="af4b9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af4b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4b9-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4b9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4b9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af4b9-130">INPUTS</span></span>

### <span data-ttu-id="af4b9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="af4b9-131">System.String</span></span>

### <span data-ttu-id="af4b9-132">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="af4b9-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="af4b9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af4b9-133">OUTPUTS</span></span>

### <span data-ttu-id="af4b9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="af4b9-134">System.String</span></span>

## <span data-ttu-id="af4b9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af4b9-135">NOTES</span></span>

## <span data-ttu-id="af4b9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af4b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="af4b9-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af4b9-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="af4b9-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="af4b9-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


