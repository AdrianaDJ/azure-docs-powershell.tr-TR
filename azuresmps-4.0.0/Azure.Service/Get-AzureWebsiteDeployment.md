---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106509"
---
# <span data-ttu-id="9c185-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="9c185-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="9c185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c185-102">SYNOPSIS</span></span>
<span data-ttu-id="9c185-103">Web sitesi için dağıtımları alır.</span><span class="sxs-lookup"><span data-stu-id="9c185-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="9c185-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c185-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c185-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c185-105">DESCRIPTION</span></span>
<span data-ttu-id="9c185-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9c185-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9c185-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9c185-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9c185-108">Azure 'daki bir Web sitesinin dağıtımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9c185-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="9c185-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c185-109">EXAMPLES</span></span>

## <span data-ttu-id="9c185-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c185-110">PARAMETERS</span></span>

### <span data-ttu-id="9c185-111">-Commid</span><span class="sxs-lookup"><span data-stu-id="9c185-111">-CommitId</span></span>
<span data-ttu-id="9c185-112">Dağıtımın benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c185-112">Specifies the unique ID for the deployment.</span></span>

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

### <span data-ttu-id="9c185-113">-Ayrıntılar</span><span class="sxs-lookup"><span data-stu-id="9c185-113">-Details</span></span>
<span data-ttu-id="9c185-114">Dağıtımlar hakkında ayrıntılı bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c185-114">Shows detailed information about the deployments.</span></span>

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

### <span data-ttu-id="9c185-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="9c185-115">-MaxResults</span></span>
<span data-ttu-id="9c185-116">Komutun döndürmesini istediğiniz en büyük sonuç sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c185-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c185-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c185-117">-Name</span></span>
<span data-ttu-id="9c185-118">Dağıtım bilgilerini almak istediğiniz Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c185-118">Specifies the name of the website for which you want to get deployment information.</span></span>

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

### <span data-ttu-id="9c185-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="9c185-119">-Profile</span></span>
<span data-ttu-id="9c185-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c185-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c185-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9c185-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c185-122">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="9c185-122">-Slot</span></span>
<span data-ttu-id="9c185-123">Yuva adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c185-123">Specifies the slot name.</span></span>

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

### <span data-ttu-id="9c185-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c185-124">CommonParameters</span></span>
<span data-ttu-id="9c185-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c185-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c185-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c185-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c185-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c185-127">INPUTS</span></span>

## <span data-ttu-id="9c185-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c185-128">OUTPUTS</span></span>

## <span data-ttu-id="9c185-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c185-129">NOTES</span></span>

## <span data-ttu-id="9c185-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c185-130">RELATED LINKS</span></span>

[<span data-ttu-id="9c185-131">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="9c185-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


