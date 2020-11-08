---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266439"
---
# <span data-ttu-id="35aac-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="35aac-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="35aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35aac-102">SYNOPSIS</span></span>
<span data-ttu-id="35aac-103">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="35aac-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="35aac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35aac-104">SYNTAX</span></span>

### <span data-ttu-id="35aac-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35aac-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35aac-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="35aac-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35aac-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35aac-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35aac-108">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="35aac-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35aac-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="35aac-109">DESCRIPTION</span></span>
<span data-ttu-id="35aac-110">Azure Active Directory uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="35aac-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="35aac-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35aac-111">EXAMPLES</span></span>

### <span data-ttu-id="35aac-112">Örnek 1: nesne kimliğini kullanarak uygulamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="35aac-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="35aac-113">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı kiracıya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="35aac-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="35aac-114">Örnek 2: uygulama kimliğine göre uygulamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="35aac-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="35aac-115">Uygulama kimliği ' f9c5ea4f-28f0-401A-A491-491a037fa346 ' olan uygulamayı kiracı 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="35aac-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="35aac-116">Örnek 3: boruları kullanarak uygulamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="35aac-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="35aac-117">Nesne kimliği ' b4cd1619-80b3-4CFB-9f8f-9f2333425738 ' olan uygulamayı ve uygulamayı kiracıdan kaldırmak için Remove-AzADApplication cmdlet 'ine sahip uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="35aac-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="35aac-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35aac-118">PARAMETERS</span></span>

### <span data-ttu-id="35aac-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="35aac-119">-ApplicationId</span></span>
<span data-ttu-id="35aac-120">Kaldırılacak uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="35aac-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="35aac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35aac-121">-DefaultProfile</span></span>
<span data-ttu-id="35aac-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="35aac-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35aac-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="35aac-123">-DisplayName</span></span>
<span data-ttu-id="35aac-124">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="35aac-124">The display name of the application.</span></span>

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

### <span data-ttu-id="35aac-125">-Force</span><span class="sxs-lookup"><span data-stu-id="35aac-125">-Force</span></span>
<span data-ttu-id="35aac-126">Onaysız uygulamayı silme düğmesi.</span><span class="sxs-lookup"><span data-stu-id="35aac-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="35aac-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35aac-127">-InputObject</span></span>
<span data-ttu-id="35aac-128">Kaldırılacak uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="35aac-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="35aac-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="35aac-129">-ObjectId</span></span>
<span data-ttu-id="35aac-130">Silinecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="35aac-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="35aac-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="35aac-131">-PassThru</span></span>
<span data-ttu-id="35aac-132">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="35aac-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="35aac-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="35aac-133">-Confirm</span></span>
<span data-ttu-id="35aac-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35aac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35aac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35aac-135">-WhatIf</span></span>
<span data-ttu-id="35aac-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35aac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35aac-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35aac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35aac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35aac-138">CommonParameters</span></span>
<span data-ttu-id="35aac-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35aac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35aac-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="35aac-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35aac-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35aac-141">INPUTS</span></span>

### <span data-ttu-id="35aac-142">System. String</span><span class="sxs-lookup"><span data-stu-id="35aac-142">System.String</span></span>

### <span data-ttu-id="35aac-143">System. Guid</span><span class="sxs-lookup"><span data-stu-id="35aac-143">System.Guid</span></span>

### <span data-ttu-id="35aac-144">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="35aac-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="35aac-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35aac-145">OUTPUTS</span></span>

### <span data-ttu-id="35aac-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35aac-146">System.Boolean</span></span>

## <span data-ttu-id="35aac-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35aac-147">NOTES</span></span>
<span data-ttu-id="35aac-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="35aac-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="35aac-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35aac-149">RELATED LINKS</span></span>

[<span data-ttu-id="35aac-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="35aac-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="35aac-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="35aac-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="35aac-152">Güncelleştirme-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="35aac-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="35aac-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="35aac-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

