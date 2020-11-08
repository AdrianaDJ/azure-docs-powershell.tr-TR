---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 6c885f4962734bf1034256843258f4755a9b3b44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275007"
---
# <span data-ttu-id="6ebc6-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="6ebc6-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="6ebc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ebc6-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebc6-103">ApplicationGroup öğesini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="6ebc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ebc6-104">SYNTAX</span></span>

### <span data-ttu-id="6ebc6-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ebc6-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6ebc6-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="6ebc6-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ebc6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ebc6-107">DESCRIPTION</span></span>
<span data-ttu-id="6ebc6-108">ApplicationGroup öğesini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="6ebc6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ebc6-109">EXAMPLES</span></span>

### <span data-ttu-id="6ebc6-110">Örnek 1: Windows sanal masaüstü ApplicationGroup adını adıyla silme</span><span class="sxs-lookup"><span data-stu-id="6ebc6-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="6ebc6-111">Bu komut, kaynak grubundaki Windows sanal masaüstü ApplicationGroup grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="6ebc6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ebc6-112">PARAMETERS</span></span>

### <span data-ttu-id="6ebc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebc6-113">-DefaultProfile</span></span>
<span data-ttu-id="6ebc6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ebc6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ebc6-115">-InputObject</span></span>
<span data-ttu-id="6ebc6-116">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6ebc6-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ebc6-117">-Name</span></span>
<span data-ttu-id="6ebc6-118">Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebc6-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6ebc6-119">-PassThru</span></span>
<span data-ttu-id="6ebc6-120">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="6ebc6-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6ebc6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebc6-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ebc6-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-122">The name of the resource group.</span></span>
<span data-ttu-id="6ebc6-123">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6ebc6-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6ebc6-124">-SubscriptionId</span></span>
<span data-ttu-id="6ebc6-125">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6ebc6-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ebc6-126">-Confirm</span></span>
<span data-ttu-id="6ebc6-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ebc6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebc6-128">-WhatIf</span></span>
<span data-ttu-id="6ebc6-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ebc6-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ebc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebc6-131">CommonParameters</span></span>
<span data-ttu-id="6ebc6-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebc6-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebc6-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ebc6-134">INPUTS</span></span>

### <span data-ttu-id="6ebc6-135">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="6ebc6-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6ebc6-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ebc6-136">OUTPUTS</span></span>

### <span data-ttu-id="6ebc6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ebc6-137">System.Boolean</span></span>

## <span data-ttu-id="6ebc6-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ebc6-138">NOTES</span></span>

<span data-ttu-id="6ebc6-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6ebc6-139">ALIASES</span></span>

<span data-ttu-id="6ebc6-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6ebc6-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ebc6-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ebc6-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ebc6-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="6ebc6-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ebc6-144">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6ebc6-145">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6ebc6-146">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6ebc6-147">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6ebc6-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="6ebc6-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ebc6-149">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6ebc6-150">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="6ebc6-151">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6ebc6-152">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6ebc6-153">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6ebc6-154">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="6ebc6-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6ebc6-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ebc6-155">RELATED LINKS</span></span>

