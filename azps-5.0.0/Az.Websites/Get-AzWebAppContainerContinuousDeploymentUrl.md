---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323485"
---
# <span data-ttu-id="a0117-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="a0117-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="a0117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0117-102">SYNOPSIS</span></span>
<span data-ttu-id="a0117-103">Get-AzWebAppContainerContinuousDeploymentUrl kapsayıcı sürekli dağıtım URL 'si geri döndürülecek</span><span class="sxs-lookup"><span data-stu-id="a0117-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="a0117-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0117-104">SYNTAX</span></span>

### <span data-ttu-id="a0117-105">S1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0117-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0117-106">S2</span><span class="sxs-lookup"><span data-stu-id="a0117-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0117-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0117-107">DESCRIPTION</span></span>
<span data-ttu-id="a0117-108">Get-AzWebAppContainerContinuousDeploymentUrl kapsayıcı sürekli dağıtım URL 'si geri döndürülecek</span><span class="sxs-lookup"><span data-stu-id="a0117-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="a0117-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0117-109">EXAMPLES</span></span>

### <span data-ttu-id="a0117-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0117-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="a0117-111">Bu komut kapsayıcı sürekli dağıtım URL 'si döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0117-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="a0117-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0117-112">PARAMETERS</span></span>

### <span data-ttu-id="a0117-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0117-113">-DefaultProfile</span></span>
<span data-ttu-id="a0117-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0117-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0117-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0117-115">-Name</span></span>
<span data-ttu-id="a0117-116">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="a0117-116">The name of the web app.</span></span>

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

### <span data-ttu-id="a0117-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0117-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0117-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a0117-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0117-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a0117-119">-SlotName</span></span>
<span data-ttu-id="a0117-120">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="a0117-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0117-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a0117-121">-WebApp</span></span>
<span data-ttu-id="a0117-122">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="a0117-122">The web app object</span></span>

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

### <span data-ttu-id="a0117-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0117-123">CommonParameters</span></span>
<span data-ttu-id="a0117-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0117-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0117-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0117-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0117-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0117-126">INPUTS</span></span>

### <span data-ttu-id="a0117-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a0117-127">System.String</span></span>

### <span data-ttu-id="a0117-128">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="a0117-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a0117-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0117-129">OUTPUTS</span></span>

### <span data-ttu-id="a0117-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a0117-130">System.String</span></span>

## <span data-ttu-id="a0117-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0117-131">NOTES</span></span>

## <span data-ttu-id="a0117-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0117-132">RELATED LINKS</span></span>
