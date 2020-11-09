---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325411"
---
# <span data-ttu-id="c8f3b-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="c8f3b-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="c8f3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f3b-103">Kubectl, Kubernetes komut satırı aracını indirin ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="c8f3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8f3b-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8f3b-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f3b-106">Kubectl, Kubernetes komut satırı aracını indirin ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="c8f3b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8f3b-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f3b-108">Kubectl 'nin en son sürümünü indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="c8f3b-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="c8f3b-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8f3b-109">PARAMETERS</span></span>

### <span data-ttu-id="c8f3b-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="c8f3b-110">-AsJob</span></span>
<span data-ttu-id="c8f3b-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c8f3b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8f3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f3b-112">-DefaultProfile</span></span>
<span data-ttu-id="c8f3b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f3b-114">-Hedef</span><span class="sxs-lookup"><span data-stu-id="c8f3b-114">-Destination</span></span>
<span data-ttu-id="c8f3b-115">Kubectl 'nin yükleneceği yol.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="c8f3b-116">Varsayılan olarak ~/.Azure-kubectl/uygulamasına yüklenecek</span><span class="sxs-lookup"><span data-stu-id="c8f3b-116">Default to install into ~/.azure-kubectl/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f3b-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="c8f3b-117">-DownloadFromMirror</span></span>
<span data-ttu-id="c8f3b-118">Yansıtma sitesinden indirin: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="c8f3b-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="c8f3b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c8f3b-119">-Force</span></span>
<span data-ttu-id="c8f3b-120">Sormadan mevcut kubectl 'nin üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="c8f3b-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="c8f3b-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c8f3b-121">-PassThru</span></span>
<span data-ttu-id="c8f3b-122">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c8f3b-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c8f3b-123">-Version</span><span class="sxs-lookup"><span data-stu-id="c8f3b-123">-Version</span></span>
<span data-ttu-id="c8f3b-124">' V 1.17.2 ' gibi bir yüklenecek kubectl sürümü.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="c8f3b-125">Varsayılan değer: en son</span><span class="sxs-lookup"><span data-stu-id="c8f3b-125">Default value: Latest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f3b-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c8f3b-126">-Confirm</span></span>
<span data-ttu-id="c8f3b-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f3b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f3b-128">-WhatIf</span></span>
<span data-ttu-id="c8f3b-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8f3b-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f3b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f3b-131">CommonParameters</span></span>
<span data-ttu-id="c8f3b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f3b-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c8f3b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f3b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8f3b-134">INPUTS</span></span>

### <span data-ttu-id="c8f3b-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c8f3b-135">None</span></span>

## <span data-ttu-id="c8f3b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8f3b-136">OUTPUTS</span></span>

### <span data-ttu-id="c8f3b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8f3b-137">System.Boolean</span></span>

## <span data-ttu-id="c8f3b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8f3b-138">NOTES</span></span>

## <span data-ttu-id="c8f3b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8f3b-139">RELATED LINKS</span></span>
