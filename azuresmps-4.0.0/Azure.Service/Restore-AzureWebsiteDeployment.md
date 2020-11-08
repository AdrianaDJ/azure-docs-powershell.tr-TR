---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105463"
---
# <span data-ttu-id="7dddf-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="7dddf-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="7dddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dddf-102">SYNOPSIS</span></span>
<span data-ttu-id="7dddf-103">Bir Web sitesinin önceki dağıtımını Azure 'da yeniden dağıtır.</span><span class="sxs-lookup"><span data-stu-id="7dddf-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="7dddf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7dddf-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dddf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7dddf-105">DESCRIPTION</span></span>
<span data-ttu-id="7dddf-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7dddf-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7dddf-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7dddf-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7dddf-108">**Restore-AzureWebsiteDeployment** cmdlet 'ı, Azure 'da bir Web sitesinin önceki dağıtımını geri dağıtır.</span><span class="sxs-lookup"><span data-stu-id="7dddf-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="7dddf-109">Bu işlem geçerli dağıtımı seçili dağıtımla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7dddf-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="7dddf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7dddf-110">EXAMPLES</span></span>

### <span data-ttu-id="7dddf-111">Örnek 1: siteyi yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="7dddf-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="7dddf-112">Bu komut, ContosoSite adlı Web sitesi için KIMLIĞI f876543210 olan dağıtımı yeniden dağıtır.</span><span class="sxs-lookup"><span data-stu-id="7dddf-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="7dddf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7dddf-113">PARAMETERS</span></span>

### <span data-ttu-id="7dddf-114">-Commid</span><span class="sxs-lookup"><span data-stu-id="7dddf-114">-CommitId</span></span>
<span data-ttu-id="7dddf-115">Dağıtımın tanımlayıcısını yeniden dağıtmak için belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dddf-115">Specifies the identifier of the deployment to redeploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dddf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7dddf-116">-Force</span></span>
<span data-ttu-id="7dddf-117">Etkinse, onay istemeden önceki dağıtımı yeniden dağıtır.</span><span class="sxs-lookup"><span data-stu-id="7dddf-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7dddf-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7dddf-118">-Name</span></span>
<span data-ttu-id="7dddf-119">Yeniden dağıtmak istediğiniz Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dddf-119">Specifies the name of the website to redeploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dddf-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="7dddf-120">-Profile</span></span>
<span data-ttu-id="7dddf-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dddf-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7dddf-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7dddf-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dddf-123">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="7dddf-123">-Slot</span></span>
<span data-ttu-id="7dddf-124">Yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dddf-124">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dddf-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="7dddf-125">-Confirm</span></span>
<span data-ttu-id="7dddf-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7dddf-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dddf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dddf-127">-WhatIf</span></span>
<span data-ttu-id="7dddf-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7dddf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dddf-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7dddf-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dddf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dddf-130">CommonParameters</span></span>
<span data-ttu-id="7dddf-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7dddf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dddf-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dddf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dddf-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7dddf-133">INPUTS</span></span>

## <span data-ttu-id="7dddf-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7dddf-134">OUTPUTS</span></span>

## <span data-ttu-id="7dddf-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7dddf-135">NOTES</span></span>

## <span data-ttu-id="7dddf-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7dddf-136">RELATED LINKS</span></span>

[<span data-ttu-id="7dddf-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7dddf-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="7dddf-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="7dddf-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


