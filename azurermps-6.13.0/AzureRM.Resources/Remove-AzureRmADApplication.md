---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 766b4d3bd135295cddf3dd0c143519c3dde50b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588368"
---
# <span data-ttu-id="07bf3-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="07bf3-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="07bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="07bf3-103">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="07bf3-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07bf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07bf3-104">SYNTAX</span></span>

### <span data-ttu-id="07bf3-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07bf3-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bf3-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="07bf3-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bf3-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07bf3-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bf3-108">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="07bf3-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07bf3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="07bf3-109">DESCRIPTION</span></span>
<span data-ttu-id="07bf3-110">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="07bf3-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="07bf3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07bf3-111">EXAMPLES</span></span>

### <span data-ttu-id="07bf3-112">Örnek 1-uygulamayı nesne kimliğiyle kaldır</span><span class="sxs-lookup"><span data-stu-id="07bf3-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="07bf3-113">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı kiracıya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07bf3-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="07bf3-114">Örnek 2-uygulama kimliğine göre uygulamayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="07bf3-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="07bf3-115">Uygulama kimliği ' f9c5ea4f-28f0-401A-A491-491a037fa346 ' olan uygulamayı kiracı 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="07bf3-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="07bf3-116">Örnek 3-şeridi kullanarak uygulamayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="07bf3-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="07bf3-117">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı ve uygulamayı kiracıdan kaldırmak için Remove-AzureRmADApplication cmdlet 'ine sahip uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="07bf3-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="07bf3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07bf3-118">PARAMETERS</span></span>

### <span data-ttu-id="07bf3-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="07bf3-119">-ApplicationId</span></span>
<span data-ttu-id="07bf3-120">Kaldırılacak uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="07bf3-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="07bf3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bf3-121">-DefaultProfile</span></span>
<span data-ttu-id="07bf3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="07bf3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07bf3-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="07bf3-123">-DisplayName</span></span>
<span data-ttu-id="07bf3-124">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="07bf3-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07bf3-125">-Force</span><span class="sxs-lookup"><span data-stu-id="07bf3-125">-Force</span></span>
<span data-ttu-id="07bf3-126">Onaysız uygulamayı silme düğmesi.</span><span class="sxs-lookup"><span data-stu-id="07bf3-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="07bf3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07bf3-127">-InputObject</span></span>
<span data-ttu-id="07bf3-128">Kaldırılacak uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="07bf3-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07bf3-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="07bf3-129">-ObjectId</span></span>
<span data-ttu-id="07bf3-130">Silinecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="07bf3-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07bf3-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="07bf3-131">-PassThru</span></span>
<span data-ttu-id="07bf3-132">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="07bf3-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="07bf3-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="07bf3-133">-Confirm</span></span>
<span data-ttu-id="07bf3-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07bf3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07bf3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bf3-135">-WhatIf</span></span>
<span data-ttu-id="07bf3-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07bf3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07bf3-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07bf3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07bf3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bf3-138">CommonParameters</span></span>
<span data-ttu-id="07bf3-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07bf3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bf3-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bf3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bf3-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07bf3-141">INPUTS</span></span>

### <span data-ttu-id="07bf3-142">System. Guid</span><span class="sxs-lookup"><span data-stu-id="07bf3-142">System.Guid</span></span>

### <span data-ttu-id="07bf3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="07bf3-143">System.String</span></span>

### <span data-ttu-id="07bf3-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="07bf3-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="07bf3-145">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="07bf3-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="07bf3-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07bf3-146">OUTPUTS</span></span>

### <span data-ttu-id="07bf3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07bf3-147">System.Boolean</span></span>

## <span data-ttu-id="07bf3-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07bf3-148">NOTES</span></span>
<span data-ttu-id="07bf3-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="07bf3-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="07bf3-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07bf3-150">RELATED LINKS</span></span>

[<span data-ttu-id="07bf3-151">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="07bf3-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="07bf3-152">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="07bf3-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="07bf3-153">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="07bf3-153">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="07bf3-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="07bf3-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

