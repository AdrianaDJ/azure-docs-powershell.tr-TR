---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108679"
---
# <span data-ttu-id="0731c-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0731c-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="0731c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0731c-102">SYNOPSIS</span></span>
<span data-ttu-id="0731c-103">SQL yönetilen örneği için Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0731c-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="0731c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0731c-104">SYNTAX</span></span>

### <span data-ttu-id="0731c-105">Useresourcegroupandınstancenameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0731c-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0731c-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0731c-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0731c-107">Userresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0731c-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0731c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0731c-108">DESCRIPTION</span></span>
<span data-ttu-id="0731c-109">**Get-Azsqlınstanceactivedirectoryadministrator** cmdlet 'i, geçerli abonelikteki bir AzureSQL yönetilen örneği Için Azure Active Directory (Azure AD) Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0731c-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="0731c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0731c-110">EXAMPLES</span></span>

### <span data-ttu-id="0731c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0731c-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="0731c-112">Bu komut, ResourceGroup01 adlı bir kaynak grubuyla ilişkilendirilmiş ManagedInstance01 adındaki yönetilen örnek için bir Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0731c-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="0731c-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0731c-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="0731c-114">Bu komut, yönetilen örnek nesnesinden Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0731c-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="0731c-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0731c-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="0731c-116">Bu komut yönetilen örnek kaynak tanımlayıcısını kullanarak Azure AD Yöneticisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0731c-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="0731c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0731c-117">PARAMETERS</span></span>

### <span data-ttu-id="0731c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0731c-118">-DefaultProfile</span></span>
<span data-ttu-id="0731c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0731c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0731c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0731c-120">-InputObject</span></span>
<span data-ttu-id="0731c-121">Kullanılacak yönetilen örnek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0731c-121">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0731c-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0731c-122">-InstanceName</span></span>
<span data-ttu-id="0731c-123">SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="0731c-123">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0731c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0731c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0731c-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0731c-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0731c-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0731c-126">-ResourceId</span></span>
<span data-ttu-id="0731c-127">Kullanılacak örneğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0731c-127">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0731c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0731c-128">CommonParameters</span></span>
<span data-ttu-id="0731c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0731c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0731c-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0731c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0731c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0731c-131">INPUTS</span></span>

### <span data-ttu-id="0731c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0731c-132">System.String</span></span>

## <span data-ttu-id="0731c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0731c-133">OUTPUTS</span></span>

### <span data-ttu-id="0731c-134">Microsoft. Azure. Commands. Sql. ınstanceactivedirectoryadministrator. model. Azuresdınstanceactivedirectoryadministratormodel</span><span class="sxs-lookup"><span data-stu-id="0731c-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="0731c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0731c-135">NOTES</span></span>

## <span data-ttu-id="0731c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0731c-136">RELATED LINKS</span></span>

[<span data-ttu-id="0731c-137">Set-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="0731c-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="0731c-138">Remove-Azsqlınstanceactivedirectoryadministrator</span><span class="sxs-lookup"><span data-stu-id="0731c-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
