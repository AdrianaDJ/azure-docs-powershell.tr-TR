---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268618"
---
# <span data-ttu-id="7a92f-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="7a92f-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="7a92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a92f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a92f-103">Belirli bir sitede veya yuvada ve belirli bir kaynak grubunda belirtilen Windows kapsayıcısında bir uzak PowerShell oturumu açar</span><span class="sxs-lookup"><span data-stu-id="7a92f-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="7a92f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a92f-104">SYNTAX</span></span>

### <span data-ttu-id="7a92f-105">S1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a92f-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a92f-106">S2</span><span class="sxs-lookup"><span data-stu-id="7a92f-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a92f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a92f-107">DESCRIPTION</span></span>
<span data-ttu-id="7a92f-108">belirli bir sitede veya yuvada ve belirli bir kaynak grubunda belirtilen Windows kapsayıcısında bir uzak PowerShell oturumu açar</span><span class="sxs-lookup"><span data-stu-id="7a92f-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="7a92f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a92f-109">EXAMPLES</span></span>

### <span data-ttu-id="7a92f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7a92f-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="7a92f-111">Bu komut Windows kapsayıcı uygulamasında bir uzak PowerShell oturumu açar ContosoASP</span><span class="sxs-lookup"><span data-stu-id="7a92f-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="7a92f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a92f-112">PARAMETERS</span></span>

### <span data-ttu-id="7a92f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a92f-113">-DefaultProfile</span></span>
<span data-ttu-id="7a92f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a92f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a92f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a92f-115">-Force</span></span>
<span data-ttu-id="7a92f-116">Onay istemeden PowerShell oturumu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7a92f-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7a92f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a92f-117">-Name</span></span>
<span data-ttu-id="7a92f-118">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="7a92f-118">The name of the web app.</span></span>

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

### <span data-ttu-id="7a92f-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7a92f-119">-PassThru</span></span>
<span data-ttu-id="7a92f-120">Başarı veya başarısızlığı belirten bir değer döndürür</span><span class="sxs-lookup"><span data-stu-id="7a92f-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="7a92f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a92f-121">-ResourceGroupName</span></span>
<span data-ttu-id="7a92f-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7a92f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a92f-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="7a92f-123">-SlotName</span></span>
<span data-ttu-id="7a92f-124">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="7a92f-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="7a92f-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7a92f-125">-WebApp</span></span>
<span data-ttu-id="7a92f-126">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a92f-126">The web app object</span></span>

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

### <span data-ttu-id="7a92f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a92f-127">-Confirm</span></span>
<span data-ttu-id="7a92f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7a92f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a92f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a92f-129">-WhatIf</span></span>
<span data-ttu-id="7a92f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a92f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a92f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a92f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a92f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a92f-132">CommonParameters</span></span>
<span data-ttu-id="7a92f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a92f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a92f-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a92f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a92f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a92f-135">INPUTS</span></span>

### <span data-ttu-id="7a92f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7a92f-136">System.String</span></span>

### <span data-ttu-id="7a92f-137">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="7a92f-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7a92f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a92f-138">OUTPUTS</span></span>

### <span data-ttu-id="7a92f-139">System. void</span><span class="sxs-lookup"><span data-stu-id="7a92f-139">System.Void</span></span>

## <span data-ttu-id="7a92f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a92f-140">NOTES</span></span>

## <span data-ttu-id="7a92f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a92f-141">RELATED LINKS</span></span>
