---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108315"
---
# <span data-ttu-id="bb39f-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="bb39f-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="bb39f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb39f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb39f-103">Kullanıcıya ileti gönderme.</span><span class="sxs-lookup"><span data-stu-id="bb39f-103">Send a message to a user.</span></span>

## <span data-ttu-id="bb39f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb39f-104">SYNTAX</span></span>

### <span data-ttu-id="bb39f-105">SendExpanded (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb39f-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb39f-106">Sendviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="bb39f-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb39f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb39f-107">DESCRIPTION</span></span>
<span data-ttu-id="bb39f-108">Kullanıcıya ileti gönderme.</span><span class="sxs-lookup"><span data-stu-id="bb39f-108">Send a message to a user.</span></span>

## <span data-ttu-id="bb39f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb39f-109">EXAMPLES</span></span>

### <span data-ttu-id="bb39f-110">Örnek 1: Kullanıcı oturumuna ileti gönderme</span><span class="sxs-lookup"><span data-stu-id="bb39f-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="bb39f-111">Bu komut bir kullanıcı oturumuna ileti gönderir.</span><span class="sxs-lookup"><span data-stu-id="bb39f-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="bb39f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb39f-112">PARAMETERS</span></span>

### <span data-ttu-id="bb39f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb39f-113">-DefaultProfile</span></span>
<span data-ttu-id="bb39f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb39f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb39f-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="bb39f-115">-HostPoolName</span></span>
<span data-ttu-id="bb39f-116">Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb39f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb39f-117">-InputObject</span></span>
<span data-ttu-id="bb39f-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bb39f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb39f-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="bb39f-119">-MessageBody</span></span>
<span data-ttu-id="bb39f-120">İleti gövdesi.</span><span class="sxs-lookup"><span data-stu-id="bb39f-120">Body of message.</span></span>

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

### <span data-ttu-id="bb39f-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="bb39f-121">-MessageTitle</span></span>
<span data-ttu-id="bb39f-122">İletinin başlığı.</span><span class="sxs-lookup"><span data-stu-id="bb39f-122">Title of message.</span></span>

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

### <span data-ttu-id="bb39f-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bb39f-123">-PassThru</span></span>
<span data-ttu-id="bb39f-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="bb39f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bb39f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb39f-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb39f-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bb39f-126">The name of the resource group.</span></span>
<span data-ttu-id="bb39f-127">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bb39f-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb39f-128">-Sessionanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="bb39f-128">-SessionHostName</span></span>
<span data-ttu-id="bb39f-129">Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb39f-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="bb39f-130">-SubscriptionId</span></span>
<span data-ttu-id="bb39f-131">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bb39f-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb39f-132">-Usersessionıd</span><span class="sxs-lookup"><span data-stu-id="bb39f-132">-UserSessionId</span></span>
<span data-ttu-id="bb39f-133">Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb39f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb39f-134">-Confirm</span></span>
<span data-ttu-id="bb39f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb39f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb39f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb39f-136">-WhatIf</span></span>
<span data-ttu-id="bb39f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb39f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb39f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb39f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb39f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb39f-139">CommonParameters</span></span>
<span data-ttu-id="bb39f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb39f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb39f-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb39f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb39f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb39f-142">INPUTS</span></span>

### <span data-ttu-id="bb39f-143">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. ıdesktopvirtualizationıdentity</span><span class="sxs-lookup"><span data-stu-id="bb39f-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bb39f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb39f-144">OUTPUTS</span></span>

### <span data-ttu-id="bb39f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb39f-145">System.Boolean</span></span>

## <span data-ttu-id="bb39f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb39f-146">NOTES</span></span>

<span data-ttu-id="bb39f-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="bb39f-147">ALIASES</span></span>

<span data-ttu-id="bb39f-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="bb39f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb39f-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bb39f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb39f-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb39f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb39f-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="bb39f-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb39f-152">`[ApplicationGroupName <String>]`: Uygulama grubunun adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bb39f-153">`[ApplicationName <String>]`: Belirtilen uygulama grubundaki uygulamanın adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bb39f-154">`[DesktopName <String>]`: Belirtilen masaüstü grubundaki masaüstünün adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bb39f-155">`[HostPoolName <String>]`: Belirtilen kaynak grubundaki konak havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bb39f-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="bb39f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb39f-157">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bb39f-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bb39f-158">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bb39f-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="bb39f-159">`[SessionHostName <String>]`: Belirtilen konak havuzundaki oturum ana bilgisayarının adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bb39f-160">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bb39f-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bb39f-161">`[UserSessionId <String>]`: Belirtilen oturum ana bilgisayarındaki kullanıcı oturumunun adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bb39f-162">`[WorkspaceName <String>]`: Çalışma alanının adı</span><span class="sxs-lookup"><span data-stu-id="bb39f-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bb39f-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb39f-163">RELATED LINKS</span></span>

