---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268602"
---
# <span data-ttu-id="97c71-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="97c71-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="97c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c71-102">SYNOPSIS</span></span>
<span data-ttu-id="97c71-103">New-AzWebAppContainerPSSession, belirli bir sitede veya yuvada ve belirli bir kaynak grubunda belirtilen Windows kapsayıcısında yeni uzak PowerShell oturumu oluşturur</span><span class="sxs-lookup"><span data-stu-id="97c71-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="97c71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97c71-104">SYNTAX</span></span>

### <span data-ttu-id="97c71-105">S1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97c71-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c71-106">S2</span><span class="sxs-lookup"><span data-stu-id="97c71-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c71-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="97c71-107">DESCRIPTION</span></span>
<span data-ttu-id="97c71-108">New-AzWebAppContainerPSSession, belirli bir sitede veya yuvada ve belirli bir kaynak grubunda belirtilen Windows kapsayıcısında yeni uzak PowerShell oturumu oluşturur</span><span class="sxs-lookup"><span data-stu-id="97c71-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="97c71-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97c71-109">EXAMPLES</span></span>

### <span data-ttu-id="97c71-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="97c71-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="97c71-111">Bu işlem, Windows kapsayıcı uygulamasında yeni bir uzak PowerShell oturumu oluşturur ve bir</span><span class="sxs-lookup"><span data-stu-id="97c71-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="97c71-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97c71-112">PARAMETERS</span></span>

### <span data-ttu-id="97c71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c71-113">-DefaultProfile</span></span>
<span data-ttu-id="97c71-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97c71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c71-115">-Force</span><span class="sxs-lookup"><span data-stu-id="97c71-115">-Force</span></span>
<span data-ttu-id="97c71-116">Onay istemeden PowerShell oturumu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="97c71-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="97c71-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="97c71-117">-Name</span></span>
<span data-ttu-id="97c71-118">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="97c71-118">The name of the web app.</span></span>

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

### <span data-ttu-id="97c71-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c71-119">-ResourceGroupName</span></span>
<span data-ttu-id="97c71-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="97c71-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="97c71-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="97c71-121">-SlotName</span></span>
<span data-ttu-id="97c71-122">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="97c71-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="97c71-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="97c71-123">-WebApp</span></span>
<span data-ttu-id="97c71-124">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="97c71-124">The web app object</span></span>

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

### <span data-ttu-id="97c71-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="97c71-125">-Confirm</span></span>
<span data-ttu-id="97c71-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97c71-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c71-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c71-127">-WhatIf</span></span>
<span data-ttu-id="97c71-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97c71-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97c71-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97c71-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c71-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c71-130">CommonParameters</span></span>
<span data-ttu-id="97c71-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97c71-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c71-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c71-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c71-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97c71-133">INPUTS</span></span>

### <span data-ttu-id="97c71-134">System. String</span><span class="sxs-lookup"><span data-stu-id="97c71-134">System.String</span></span>

### <span data-ttu-id="97c71-135">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="97c71-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="97c71-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97c71-136">OUTPUTS</span></span>

### <span data-ttu-id="97c71-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="97c71-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="97c71-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97c71-138">NOTES</span></span>

## <span data-ttu-id="97c71-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97c71-139">RELATED LINKS</span></span>
