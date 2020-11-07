---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 00c9d6e5a5a729ca5a5119b812873078acb38326
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936368"
---
# <span data-ttu-id="51e78-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="51e78-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="51e78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51e78-102">SYNOPSIS</span></span>
<span data-ttu-id="51e78-103">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="51e78-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="51e78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51e78-104">SYNTAX</span></span>

### <span data-ttu-id="51e78-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51e78-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e78-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="51e78-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e78-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="51e78-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e78-108">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="51e78-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e78-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="51e78-109">DESCRIPTION</span></span>
<span data-ttu-id="51e78-110">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="51e78-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="51e78-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51e78-111">EXAMPLES</span></span>

### <span data-ttu-id="51e78-112">Örnek 1-uygulamayı nesne kimliğiyle kaldır</span><span class="sxs-lookup"><span data-stu-id="51e78-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="51e78-113">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı kiracıya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51e78-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="51e78-114">Örnek 2-uygulama kimliğine göre uygulamayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="51e78-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="51e78-115">Uygulama kimliği ' f9c5ea4f-28f0-401A-A491-491a037fa346 ' olan uygulamayı kiracı 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51e78-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="51e78-116">Örnek 3-şeridi kullanarak uygulamayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="51e78-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="51e78-117">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı ve uygulamayı kiracıdan kaldırmak için Remove-AzADApplication cmdlet 'ine sahip uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="51e78-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="51e78-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51e78-118">PARAMETERS</span></span>

### <span data-ttu-id="51e78-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="51e78-119">-ApplicationId</span></span>
<span data-ttu-id="51e78-120">Kaldırılacak uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="51e78-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="51e78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e78-121">-DefaultProfile</span></span>
<span data-ttu-id="51e78-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="51e78-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51e78-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="51e78-123">-DisplayName</span></span>
<span data-ttu-id="51e78-124">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="51e78-124">The display name of the application.</span></span>

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

### <span data-ttu-id="51e78-125">-Force</span><span class="sxs-lookup"><span data-stu-id="51e78-125">-Force</span></span>
<span data-ttu-id="51e78-126">Onaysız uygulamayı silme düğmesi.</span><span class="sxs-lookup"><span data-stu-id="51e78-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="51e78-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51e78-127">-InputObject</span></span>
<span data-ttu-id="51e78-128">Kaldırılacak uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="51e78-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="51e78-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="51e78-129">-ObjectId</span></span>
<span data-ttu-id="51e78-130">Silinecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="51e78-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="51e78-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="51e78-131">-PassThru</span></span>
<span data-ttu-id="51e78-132">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="51e78-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="51e78-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="51e78-133">-Confirm</span></span>
<span data-ttu-id="51e78-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51e78-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e78-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e78-135">-WhatIf</span></span>
<span data-ttu-id="51e78-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51e78-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e78-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51e78-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e78-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e78-138">CommonParameters</span></span>
<span data-ttu-id="51e78-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51e78-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e78-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e78-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e78-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51e78-141">INPUTS</span></span>

### <span data-ttu-id="51e78-142">System. Guid</span><span class="sxs-lookup"><span data-stu-id="51e78-142">System.Guid</span></span>

### <span data-ttu-id="51e78-143">System. String</span><span class="sxs-lookup"><span data-stu-id="51e78-143">System.String</span></span>

### <span data-ttu-id="51e78-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="51e78-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="51e78-145">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="51e78-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="51e78-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51e78-146">OUTPUTS</span></span>

### <span data-ttu-id="51e78-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51e78-147">System.Boolean</span></span>

## <span data-ttu-id="51e78-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51e78-148">NOTES</span></span>
<span data-ttu-id="51e78-149">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="51e78-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="51e78-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51e78-150">RELATED LINKS</span></span>

[<span data-ttu-id="51e78-151">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="51e78-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="51e78-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="51e78-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="51e78-153">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="51e78-153">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="51e78-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="51e78-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

