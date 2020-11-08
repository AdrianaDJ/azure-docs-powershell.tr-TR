---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 7b0cdf0cbe0aecdb2e1b6829ed1ec22b1e485e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274556"
---
# <span data-ttu-id="41bc2-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="41bc2-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="41bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="41bc2-103">Konak havuzunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="41bc2-103">Remove a host pool.</span></span>

## <span data-ttu-id="41bc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41bc2-104">SYNTAX</span></span>

### <span data-ttu-id="41bc2-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="41bc2-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41bc2-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="41bc2-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41bc2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="41bc2-107">DESCRIPTION</span></span>
<span data-ttu-id="41bc2-108">Konak havuzunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="41bc2-108">Remove a host pool.</span></span>

## <span data-ttu-id="41bc2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41bc2-109">EXAMPLES</span></span>

### <span data-ttu-id="41bc2-110">Örnek 1: Windows sanal masaüstü HostPool adını adıyla silme</span><span class="sxs-lookup"><span data-stu-id="41bc2-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="41bc2-111">Bu komut, kaynak grubundaki Windows sanal masaüstü HostPool öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="41bc2-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="41bc2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41bc2-112">PARAMETERS</span></span>

### <span data-ttu-id="41bc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41bc2-113">-DefaultProfile</span></span>
<span data-ttu-id="41bc2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41bc2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41bc2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="41bc2-115">-Force</span></span>
<span data-ttu-id="41bc2-116">Force bayrağı sessionHost öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="41bc2-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="41bc2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41bc2-117">-InputObject</span></span>
<span data-ttu-id="41bc2-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41bc2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41bc2-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="41bc2-119">-Name</span></span>
<span data-ttu-id="41bc2-120">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bc2-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="41bc2-121">-PassThru</span></span>
<span data-ttu-id="41bc2-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="41bc2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41bc2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41bc2-123">-ResourceGroupName</span></span>
<span data-ttu-id="41bc2-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="41bc2-124">The name of the resource group.</span></span>
<span data-ttu-id="41bc2-125">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="41bc2-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bc2-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="41bc2-126">-SubscriptionId</span></span>
<span data-ttu-id="41bc2-127">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="41bc2-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bc2-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="41bc2-128">-Confirm</span></span>
<span data-ttu-id="41bc2-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="41bc2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41bc2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41bc2-130">-WhatIf</span></span>
<span data-ttu-id="41bc2-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="41bc2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41bc2-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="41bc2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41bc2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bc2-133">CommonParameters</span></span>
<span data-ttu-id="41bc2-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41bc2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bc2-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="41bc2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bc2-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41bc2-136">INPUTS</span></span>

### <span data-ttu-id="41bc2-137">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="41bc2-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="41bc2-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41bc2-138">OUTPUTS</span></span>

### <span data-ttu-id="41bc2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41bc2-139">System.Boolean</span></span>

## <span data-ttu-id="41bc2-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41bc2-140">NOTES</span></span>

<span data-ttu-id="41bc2-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="41bc2-141">ALIASES</span></span>

<span data-ttu-id="41bc2-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="41bc2-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41bc2-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="41bc2-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41bc2-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41bc2-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41bc2-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="41bc2-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41bc2-146">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="41bc2-147">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="41bc2-148">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="41bc2-149">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="41bc2-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="41bc2-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41bc2-151">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="41bc2-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="41bc2-152">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="41bc2-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="41bc2-153">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="41bc2-154">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="41bc2-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="41bc2-155">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="41bc2-156">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="41bc2-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="41bc2-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41bc2-157">RELATED LINKS</span></span>

