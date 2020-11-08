---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273929"
---
# <span data-ttu-id="48cd6-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="48cd6-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="48cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="48cd6-103">Hizmeti silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="48cd6-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="48cd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48cd6-104">SYNTAX</span></span>

### <span data-ttu-id="48cd6-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48cd6-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="48cd6-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="48cd6-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48cd6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="48cd6-107">DESCRIPTION</span></span>
<span data-ttu-id="48cd6-108">Hizmeti silme işlemi.</span><span class="sxs-lookup"><span data-stu-id="48cd6-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="48cd6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48cd6-109">EXAMPLES</span></span>

### <span data-ttu-id="48cd6-110">Örnek 1: yay bulut hizmetini adıyla kaldır.</span><span class="sxs-lookup"><span data-stu-id="48cd6-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="48cd6-111">Yay bulut hizmetini adıyla kaldır.</span><span class="sxs-lookup"><span data-stu-id="48cd6-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="48cd6-112">Örnek 2: yay bulut hizmetini kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="48cd6-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="48cd6-113">Yay bulut hizmetini kanaldan kaldır.</span><span class="sxs-lookup"><span data-stu-id="48cd6-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="48cd6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48cd6-114">PARAMETERS</span></span>

### <span data-ttu-id="48cd6-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="48cd6-115">-AsJob</span></span>
<span data-ttu-id="48cd6-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="48cd6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="48cd6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cd6-117">-DefaultProfile</span></span>
<span data-ttu-id="48cd6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48cd6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48cd6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48cd6-119">-InputObject</span></span>
<span data-ttu-id="48cd6-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48cd6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48cd6-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="48cd6-121">-Name</span></span>
<span data-ttu-id="48cd6-122">Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48cd6-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="48cd6-123">-NoWait</span></span>
<span data-ttu-id="48cd6-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="48cd6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="48cd6-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="48cd6-125">-PassThru</span></span>
<span data-ttu-id="48cd6-126">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="48cd6-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="48cd6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48cd6-127">-ResourceGroupName</span></span>
<span data-ttu-id="48cd6-128">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="48cd6-129">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="48cd6-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="48cd6-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="48cd6-130">-SubscriptionId</span></span>
<span data-ttu-id="48cd6-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="48cd6-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="48cd6-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="48cd6-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="48cd6-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="48cd6-133">-Confirm</span></span>
<span data-ttu-id="48cd6-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48cd6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48cd6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48cd6-135">-WhatIf</span></span>
<span data-ttu-id="48cd6-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48cd6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48cd6-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48cd6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48cd6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cd6-138">CommonParameters</span></span>
<span data-ttu-id="48cd6-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48cd6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cd6-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="48cd6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cd6-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48cd6-141">INPUTS</span></span>

### <span data-ttu-id="48cd6-142">Microsoft. Azure. PowerShell. cmdlet. SpringCloud. modeller. ıspringcloudidentity</span><span class="sxs-lookup"><span data-stu-id="48cd6-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="48cd6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48cd6-143">OUTPUTS</span></span>

### <span data-ttu-id="48cd6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48cd6-144">System.Boolean</span></span>

## <span data-ttu-id="48cd6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48cd6-145">NOTES</span></span>

<span data-ttu-id="48cd6-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="48cd6-146">ALIASES</span></span>

<span data-ttu-id="48cd6-147">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="48cd6-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48cd6-148">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="48cd6-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48cd6-149">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48cd6-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48cd6-150">INPUTOBJECT <ISpringCloudIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="48cd6-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48cd6-151">`[AppName <String>]`: Uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="48cd6-152">`[BindingName <String>]`: Bağlama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="48cd6-153">`[CertificateName <String>]`: Sertifika kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="48cd6-154">`[DeploymentName <String>]`: Dağıtım kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="48cd6-155">`[DomainName <String>]`: Özel etki alanı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="48cd6-156">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="48cd6-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48cd6-157">`[Location <String>]`: bölge</span><span class="sxs-lookup"><span data-stu-id="48cd6-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="48cd6-158">`[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="48cd6-159">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="48cd6-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="48cd6-160">`[ServiceName <String>]`: Hizmet kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="48cd6-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="48cd6-161">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="48cd6-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="48cd6-162">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="48cd6-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="48cd6-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48cd6-163">RELATED LINKS</span></span>

