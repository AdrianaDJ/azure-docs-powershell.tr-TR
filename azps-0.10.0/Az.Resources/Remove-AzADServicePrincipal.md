---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 966b9baf35f1719f29fda6355a9675739693314f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936364"
---
# <span data-ttu-id="c1bea-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1bea-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="c1bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1bea-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bea-103">Azure Active Directory hizmet sorumlusunu siler.</span><span class="sxs-lookup"><span data-stu-id="c1bea-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="c1bea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1bea-104">SYNTAX</span></span>

### <span data-ttu-id="c1bea-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1bea-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1bea-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c1bea-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1bea-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1bea-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1bea-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1bea-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1bea-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="c1bea-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1bea-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1bea-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1bea-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1bea-111">DESCRIPTION</span></span>
<span data-ttu-id="c1bea-112">Azure Active Directory hizmet sorumlusunu siler.</span><span class="sxs-lookup"><span data-stu-id="c1bea-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="c1bea-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1bea-113">EXAMPLES</span></span>

### <span data-ttu-id="c1bea-114">Örnek 1-nesne kimliğini kullanarak hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1bea-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="c1bea-115">Nesne kimliği ' 61b5d8ea-fdc6-40a2-8vseç5b-ad447c678vseç45 ' olan hizmet sorumlusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1bea-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="c1bea-116">Örnek 2-uygulama kimliğine göre hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1bea-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="c1bea-117">Uygulama kimliği ' 9263469e-vseç328-4321-8646-3e3e75)ile hizmet sorumlusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1bea-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="c1bea-118">Örnek 3-SPN 'nin hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1bea-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="c1bea-119">Hizmet asıl adını "MyServicePrincipal" olan hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1bea-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="c1bea-120">Örnek 4-boruları kullanarak hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1bea-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="c1bea-121">Nesne kimliği ' 61b5d8ea-fdc6-40a2-8vseç5b-ad447c678vseç45 ' ve Remove-AzADServicePrincipal yöneltme</span><span class="sxs-lookup"><span data-stu-id="c1bea-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="c1bea-122">Örnek 5-bir uygulamayı yöneltme yoluyla hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1bea-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="c1bea-123">Uygulama kimliği ' 9263469e-vseç328-4321-8646-3e3e75t7e76 Remove-AzADServicePrincipal ' ile uygulama</span><span class="sxs-lookup"><span data-stu-id="c1bea-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="c1bea-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1bea-124">PARAMETERS</span></span>

### <span data-ttu-id="c1bea-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c1bea-125">-ApplicationId</span></span>
<span data-ttu-id="c1bea-126">Hizmet sorumlusu uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="c1bea-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c1bea-127">-ApplicationObject</span></span>
<span data-ttu-id="c1bea-128">Hizmet sorumlusu kaldırılmakta olan uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c1bea-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bea-129">-DefaultProfile</span></span>
<span data-ttu-id="c1bea-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c1bea-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c1bea-131">-DisplayName</span></span>
<span data-ttu-id="c1bea-132">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="c1bea-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-133">-Force</span><span class="sxs-lookup"><span data-stu-id="c1bea-133">-Force</span></span>
<span data-ttu-id="c1bea-134">Onay olmadan hizmet sorumlusunu Sil 'e geçin.</span><span class="sxs-lookup"><span data-stu-id="c1bea-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="c1bea-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1bea-135">-InputObject</span></span>
<span data-ttu-id="c1bea-136">Hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c1bea-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-137">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c1bea-137">-ObjectId</span></span>
<span data-ttu-id="c1bea-138">Silinecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="c1bea-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-139">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c1bea-139">-PassThru</span></span>
<span data-ttu-id="c1bea-140">Belirtilmişse, silinmiş hizmet sorumlusunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="c1bea-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="c1bea-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c1bea-141">-ServicePrincipalName</span></span>
<span data-ttu-id="c1bea-142">Hizmet asıl adı.</span><span class="sxs-lookup"><span data-stu-id="c1bea-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bea-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1bea-143">-Confirm</span></span>
<span data-ttu-id="c1bea-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1bea-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1bea-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1bea-145">-WhatIf</span></span>
<span data-ttu-id="c1bea-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1bea-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1bea-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1bea-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1bea-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bea-148">CommonParameters</span></span>
<span data-ttu-id="c1bea-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1bea-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bea-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1bea-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bea-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1bea-151">INPUTS</span></span>

### <span data-ttu-id="c1bea-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c1bea-152">System.Guid</span></span>

### <span data-ttu-id="c1bea-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c1bea-153">System.String</span></span>

### <span data-ttu-id="c1bea-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1bea-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="c1bea-155">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c1bea-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c1bea-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c1bea-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="c1bea-157">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c1bea-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="c1bea-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1bea-158">OUTPUTS</span></span>

### <span data-ttu-id="c1bea-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1bea-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c1bea-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1bea-160">NOTES</span></span>
<span data-ttu-id="c1bea-161">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="c1bea-161">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c1bea-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1bea-162">RELATED LINKS</span></span>

[<span data-ttu-id="c1bea-163">Yeni-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1bea-163">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="c1bea-164">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1bea-164">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="c1bea-165">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c1bea-165">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="c1bea-166">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c1bea-166">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c1bea-167">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c1bea-167">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)