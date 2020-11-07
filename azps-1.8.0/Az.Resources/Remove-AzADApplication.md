---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: eed437a235072972778925c0b94f2d22466399b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759362"
---
# <span data-ttu-id="81177-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="81177-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="81177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81177-102">SYNOPSIS</span></span>
<span data-ttu-id="81177-103">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="81177-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="81177-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81177-104">SYNTAX</span></span>

### <span data-ttu-id="81177-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81177-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81177-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="81177-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81177-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="81177-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81177-108">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="81177-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81177-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="81177-109">DESCRIPTION</span></span>
<span data-ttu-id="81177-110">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="81177-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="81177-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81177-111">EXAMPLES</span></span>

### <span data-ttu-id="81177-112">Örnek 1-uygulamayı nesne kimliğiyle kaldır</span><span class="sxs-lookup"><span data-stu-id="81177-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="81177-113">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı kiracıya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81177-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="81177-114">Örnek 2-uygulama kimliğine göre uygulamayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="81177-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="81177-115">Uygulama kimliği ' f9c5ea4f-28f0-401A-A491-491a037fa346 ' olan uygulamayı kiracı 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81177-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="81177-116">Örnek 3-şeridi kullanarak uygulamayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="81177-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="81177-117">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı ve uygulamayı kiracıdan kaldırmak için Remove-AzADApplication cmdlet 'ine sahip uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="81177-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="81177-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81177-118">PARAMETERS</span></span>

### <span data-ttu-id="81177-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="81177-119">-ApplicationId</span></span>
<span data-ttu-id="81177-120">Kaldırılacak uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="81177-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="81177-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81177-121">-DefaultProfile</span></span>
<span data-ttu-id="81177-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="81177-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81177-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81177-123">-DisplayName</span></span>
<span data-ttu-id="81177-124">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="81177-124">The display name of the application.</span></span>

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

### <span data-ttu-id="81177-125">-Force</span><span class="sxs-lookup"><span data-stu-id="81177-125">-Force</span></span>
<span data-ttu-id="81177-126">Onaysız uygulamayı silme düğmesi.</span><span class="sxs-lookup"><span data-stu-id="81177-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="81177-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81177-127">-InputObject</span></span>
<span data-ttu-id="81177-128">Kaldırılacak uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="81177-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81177-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="81177-129">-ObjectId</span></span>
<span data-ttu-id="81177-130">Silinecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="81177-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81177-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="81177-131">-PassThru</span></span>
<span data-ttu-id="81177-132">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="81177-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="81177-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="81177-133">-Confirm</span></span>
<span data-ttu-id="81177-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81177-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81177-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81177-135">-WhatIf</span></span>
<span data-ttu-id="81177-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81177-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81177-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81177-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81177-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81177-138">CommonParameters</span></span>
<span data-ttu-id="81177-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81177-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81177-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81177-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81177-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81177-141">INPUTS</span></span>

### <span data-ttu-id="81177-142">System. String</span><span class="sxs-lookup"><span data-stu-id="81177-142">System.String</span></span>

### <span data-ttu-id="81177-143">System. Guid</span><span class="sxs-lookup"><span data-stu-id="81177-143">System.Guid</span></span>

### <span data-ttu-id="81177-144">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="81177-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="81177-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81177-145">OUTPUTS</span></span>

### <span data-ttu-id="81177-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81177-146">System.Boolean</span></span>

## <span data-ttu-id="81177-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81177-147">NOTES</span></span>
<span data-ttu-id="81177-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="81177-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="81177-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81177-149">RELATED LINKS</span></span>

[<span data-ttu-id="81177-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="81177-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="81177-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="81177-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="81177-152">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="81177-152">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="81177-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="81177-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
