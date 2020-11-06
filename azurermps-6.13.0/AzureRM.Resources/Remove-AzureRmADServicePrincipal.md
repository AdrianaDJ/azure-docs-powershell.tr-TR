---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 07bc19bd2314164b37ec9e014f5cad68de97d21f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589368"
---
# <span data-ttu-id="8b4eb-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8b4eb-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="8b4eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4eb-103">Azure Active Directory hizmet sorumlusunu siler.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b4eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b4eb-104">SYNTAX</span></span>

### <span data-ttu-id="8b4eb-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b4eb-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4eb-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8b4eb-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4eb-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4eb-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4eb-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4eb-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4eb-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="8b4eb-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4eb-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4eb-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b4eb-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b4eb-111">DESCRIPTION</span></span>
<span data-ttu-id="8b4eb-112">Azure Active Directory hizmet sorumlusunu siler.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="8b4eb-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b4eb-113">EXAMPLES</span></span>

### <span data-ttu-id="8b4eb-114">Örnek 1-nesne kimliğini kullanarak hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b4eb-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="8b4eb-115">Nesne kimliği ' 61b5d8ea-fdc6-40a2-8vseç5b-ad447c678vseç45 ' olan hizmet sorumlusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="8b4eb-116">Örnek 2-uygulama kimliğine göre hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b4eb-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="8b4eb-117">Uygulama kimliği ' 9263469e-vseç328-4321-8646-3e3e75)ile hizmet sorumlusunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="8b4eb-118">Örnek 3-SPN 'nin hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b4eb-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="8b4eb-119">Hizmet asıl adını "MyServicePrincipal" olan hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b4eb-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="8b4eb-120">Örnek 4-boruları kullanarak hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b4eb-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="8b4eb-121">Nesne kimliği ' 61b5d8ea-fdc6-40a2-8vseç5b-ad447c678vseç45 ' ve Remove-AzureRmADServicePrincipal yöneltme</span><span class="sxs-lookup"><span data-stu-id="8b4eb-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="8b4eb-122">Örnek 5-bir uygulamayı yöneltme yoluyla hizmet sorumlusunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b4eb-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="8b4eb-123">Uygulama kimliği ' 9263469e-vseç328-4321-8646-3e3e75t7e76 Remove-AzureRmADServicePrincipal ' ile uygulama</span><span class="sxs-lookup"><span data-stu-id="8b4eb-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="8b4eb-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b4eb-124">PARAMETERS</span></span>

### <span data-ttu-id="8b4eb-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8b4eb-125">-ApplicationId</span></span>
<span data-ttu-id="8b4eb-126">Hizmet sorumlusu uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-126">The service principal application id.</span></span>

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

### <span data-ttu-id="8b4eb-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8b4eb-127">-ApplicationObject</span></span>
<span data-ttu-id="8b4eb-128">Hizmet sorumlusu kaldırılmakta olan uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="8b4eb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4eb-129">-DefaultProfile</span></span>
<span data-ttu-id="8b4eb-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8b4eb-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b4eb-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8b4eb-131">-DisplayName</span></span>
<span data-ttu-id="8b4eb-132">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="8b4eb-133">-Force</span><span class="sxs-lookup"><span data-stu-id="8b4eb-133">-Force</span></span>
<span data-ttu-id="8b4eb-134">Onay olmadan hizmet sorumlusunu Sil 'e geçin.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="8b4eb-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b4eb-135">-InputObject</span></span>
<span data-ttu-id="8b4eb-136">Hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-136">The service principal object.</span></span>

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

### <span data-ttu-id="8b4eb-137">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8b4eb-137">-ObjectId</span></span>
<span data-ttu-id="8b4eb-138">Silinecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="8b4eb-139">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8b4eb-139">-PassThru</span></span>
<span data-ttu-id="8b4eb-140">Belirtilmişse, silinmiş hizmet sorumlusunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="8b4eb-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8b4eb-141">-ServicePrincipalName</span></span>
<span data-ttu-id="8b4eb-142">Hizmet asıl adı.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-142">The service principal name.</span></span>

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

### <span data-ttu-id="8b4eb-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b4eb-143">-Confirm</span></span>
<span data-ttu-id="8b4eb-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b4eb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b4eb-145">-WhatIf</span></span>
<span data-ttu-id="8b4eb-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b4eb-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b4eb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4eb-148">CommonParameters</span></span>
<span data-ttu-id="8b4eb-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b4eb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4eb-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4eb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4eb-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b4eb-151">INPUTS</span></span>

### <span data-ttu-id="8b4eb-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="8b4eb-152">System.Guid</span></span>

### <span data-ttu-id="8b4eb-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8b4eb-153">System.String</span></span>

### <span data-ttu-id="8b4eb-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8b4eb-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="8b4eb-155">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b4eb-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8b4eb-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8b4eb-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="8b4eb-157">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b4eb-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="8b4eb-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b4eb-158">OUTPUTS</span></span>

### <span data-ttu-id="8b4eb-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8b4eb-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="8b4eb-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b4eb-160">NOTES</span></span>
<span data-ttu-id="8b4eb-161">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="8b4eb-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8b4eb-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b4eb-162">RELATED LINKS</span></span>

[<span data-ttu-id="8b4eb-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8b4eb-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8b4eb-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8b4eb-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8b4eb-165">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8b4eb-165">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8b4eb-166">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8b4eb-166">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="8b4eb-167">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8b4eb-167">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
