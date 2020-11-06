---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587085"
---
# <span data-ttu-id="a4e0f-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="a4e0f-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="a4e0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e0f-103">New-AzureRmWebAppContainerPSSession, belirli bir sitede veya yuvada ve belirli bir kaynak grubunda belirtilen Windows kapsayıcısında yeni uzak PowerShell oturumu oluşturur</span><span class="sxs-lookup"><span data-stu-id="a4e0f-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4e0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4e0f-104">SYNTAX</span></span>

### <span data-ttu-id="a4e0f-105">S1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a4e0f-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4e0f-106">S2</span><span class="sxs-lookup"><span data-stu-id="a4e0f-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4e0f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4e0f-107">DESCRIPTION</span></span>
<span data-ttu-id="a4e0f-108">New-AzureRmWebAppContainerPSSession, belirli bir sitede veya yuvada ve belirli bir kaynak grubunda belirtilen Windows kapsayıcısında yeni uzak PowerShell oturumu oluşturur</span><span class="sxs-lookup"><span data-stu-id="a4e0f-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="a4e0f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4e0f-109">EXAMPLES</span></span>

### <span data-ttu-id="a4e0f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4e0f-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="a4e0f-111">Bu işlem, Windows kapsayıcı uygulamasında yeni bir uzak PowerShell oturumu oluşturur ve bir</span><span class="sxs-lookup"><span data-stu-id="a4e0f-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="a4e0f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4e0f-112">PARAMETERS</span></span>

### <span data-ttu-id="a4e0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e0f-113">-DefaultProfile</span></span>
<span data-ttu-id="a4e0f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4e0f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a4e0f-115">-Force</span></span>
<span data-ttu-id="a4e0f-116">Onay istemeden PowerShell oturumu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a4e0f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4e0f-117">-Name</span></span>
<span data-ttu-id="a4e0f-118">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a4e0f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4e0f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4e0f-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4e0f-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a4e0f-121">-SlotName</span></span>
<span data-ttu-id="a4e0f-122">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a4e0f-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a4e0f-123">-WebApp</span></span>
<span data-ttu-id="a4e0f-124">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="a4e0f-124">The web app object</span></span>

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

### <span data-ttu-id="a4e0f-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4e0f-125">-Confirm</span></span>
<span data-ttu-id="a4e0f-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4e0f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4e0f-127">-WhatIf</span></span>
<span data-ttu-id="a4e0f-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4e0f-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4e0f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e0f-130">CommonParameters</span></span>
<span data-ttu-id="a4e0f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4e0f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e0f-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e0f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e0f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4e0f-133">INPUTS</span></span>

### <span data-ttu-id="a4e0f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4e0f-134">System.String</span></span>
### <span data-ttu-id="a4e0f-135">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="a4e0f-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="a4e0f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4e0f-136">OUTPUTS</span></span>

### <span data-ttu-id="a4e0f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a4e0f-137">System.String</span></span>
## <span data-ttu-id="a4e0f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4e0f-138">NOTES</span></span>

## <span data-ttu-id="a4e0f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4e0f-139">RELATED LINKS</span></span>
