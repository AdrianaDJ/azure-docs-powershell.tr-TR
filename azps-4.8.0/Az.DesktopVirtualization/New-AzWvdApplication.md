---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274554"
---
# <span data-ttu-id="5a16a-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="5a16a-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="5a16a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a16a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a16a-103">Uygulama oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="5a16a-103">Create or update an application.</span></span>

## <span data-ttu-id="5a16a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a16a-104">SYNTAX</span></span>

### <span data-ttu-id="5a16a-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a16a-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a16a-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="5a16a-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a16a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a16a-107">DESCRIPTION</span></span>
<span data-ttu-id="5a16a-108">Uygulama oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="5a16a-108">Create or update an application.</span></span>

## <span data-ttu-id="5a16a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a16a-109">EXAMPLES</span></span>

### <span data-ttu-id="5a16a-110">Örnek 1: Windows sanal masaüstü uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a16a-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="5a16a-111">Bu komut, bir uygulama grubunda Windows sanal masaüstü uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a16a-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="5a16a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a16a-112">PARAMETERS</span></span>

### <span data-ttu-id="5a16a-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="5a16a-113">-AppAlias</span></span>
<span data-ttu-id="5a16a-114">Başlat menü öğesinden uygulama diğer adı</span><span class="sxs-lookup"><span data-stu-id="5a16a-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-115">-Commanddoğrtası</span><span class="sxs-lookup"><span data-stu-id="5a16a-115">-CommandLineArgument</span></span>
<span data-ttu-id="5a16a-116">Uygulama için komut satırı bağımsız değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="5a16a-116">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="5a16a-117">-CommandLineSetting</span></span>
<span data-ttu-id="5a16a-118">Bu yayınlanan uygulamanın, istemci tarafından sağlanan komut satırı bağımsız değişkenleriyle, yayımlama zamanında belirtilen komut satırı bağımsız değişkenleriyle mi başlatılabildiğini veya hiçbir komut satırı bağımsız değişkeni olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a16a-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a16a-119">-DefaultProfile</span></span>
<span data-ttu-id="5a16a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a16a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="5a16a-121">-Description</span></span>
<span data-ttu-id="5a16a-122">Uygulamanın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="5a16a-122">Description of Application.</span></span>

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

### <span data-ttu-id="5a16a-123">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="5a16a-123">-FilePath</span></span>
<span data-ttu-id="5a16a-124">Uygulamanın yürütülebilir dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a16a-124">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5a16a-125">-FriendlyName</span></span>
<span data-ttu-id="5a16a-126">Uygulamanın kolay adı.</span><span class="sxs-lookup"><span data-stu-id="5a16a-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="5a16a-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="5a16a-127">-GroupName</span></span>
<span data-ttu-id="5a16a-128">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5a16a-128">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-129">-Iconındex</span><span class="sxs-lookup"><span data-stu-id="5a16a-129">-IconIndex</span></span>
<span data-ttu-id="5a16a-130">Simgenin dizini.</span><span class="sxs-lookup"><span data-stu-id="5a16a-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-131">-Fıyol</span><span class="sxs-lookup"><span data-stu-id="5a16a-131">-IconPath</span></span>
<span data-ttu-id="5a16a-132">Simgenin yolu.</span><span class="sxs-lookup"><span data-stu-id="5a16a-132">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a16a-133">-Name</span></span>
<span data-ttu-id="5a16a-134">Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="5a16a-134">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a16a-135">-ResourceGroupName</span></span>
<span data-ttu-id="5a16a-136">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5a16a-136">The name of the resource group.</span></span>
<span data-ttu-id="5a16a-137">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5a16a-137">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="5a16a-138">-ShowInPortal</span></span>
<span data-ttu-id="5a16a-139">RD Web erişimi sunucusunda RemoteApp programının gösterilip gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a16a-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="5a16a-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5a16a-140">-SubscriptionId</span></span>
<span data-ttu-id="5a16a-141">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5a16a-141">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a16a-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a16a-142">-Confirm</span></span>
<span data-ttu-id="5a16a-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a16a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a16a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a16a-144">-WhatIf</span></span>
<span data-ttu-id="5a16a-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a16a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a16a-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a16a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a16a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a16a-147">CommonParameters</span></span>
<span data-ttu-id="5a16a-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a16a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a16a-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5a16a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a16a-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a16a-150">INPUTS</span></span>

## <span data-ttu-id="5a16a-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a16a-151">OUTPUTS</span></span>

### <span data-ttu-id="5a16a-152">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. ıapplication</span><span class="sxs-lookup"><span data-stu-id="5a16a-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="5a16a-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a16a-153">NOTES</span></span>

<span data-ttu-id="5a16a-154">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5a16a-154">ALIASES</span></span>

## <span data-ttu-id="5a16a-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a16a-155">RELATED LINKS</span></span>

