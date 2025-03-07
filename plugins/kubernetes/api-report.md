## API Report File for "@backstage/plugin-kubernetes"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="react" />

import { ApiRef } from '@backstage/core-plugin-api';
import { AsyncState } from 'react-use/lib/useAsyncFn';
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { ClientContainerStatus } from '@backstage/plugin-kubernetes-common';
import { ClientPodStatus } from '@backstage/plugin-kubernetes-common';
import { ClusterAttributes } from '@backstage/plugin-kubernetes-common';
import { ClusterObjects } from '@backstage/plugin-kubernetes-common';
import { CustomObjectsByEntityRequest } from '@backstage/plugin-kubernetes-common';
import { CustomResourceMatcher } from '@backstage/plugin-kubernetes-common';
import { DiscoveryApi } from '@backstage/core-plugin-api';
import { Entity } from '@backstage/catalog-model';
import { Event as Event_2 } from 'kubernetes-models/v1';
import { IContainer } from 'kubernetes-models/v1';
import { IContainerStatus } from 'kubernetes-models/v1';
import { IdentityApi } from '@backstage/core-plugin-api';
import { IIoK8sApimachineryPkgApisMetaV1ObjectMeta } from '@kubernetes-models/apimachinery/apis/meta/v1/ObjectMeta';
import { IObjectMeta } from '@kubernetes-models/apimachinery/apis/meta/v1/ObjectMeta';
import type { JsonObject } from '@backstage/types';
import { KubernetesRequestBody } from '@backstage/plugin-kubernetes-common';
import { OAuthApi } from '@backstage/core-plugin-api';
import { ObjectsByEntityResponse } from '@backstage/plugin-kubernetes-common';
import { OpenIdConnectApi } from '@backstage/core-plugin-api';
import { Pod } from 'kubernetes-models/v1/Pod';
import { Pod as Pod_2 } from 'kubernetes-models/v1';
import { default as React_2 } from 'react';
import * as React_3 from 'react';
import { RouteRef } from '@backstage/core-plugin-api';
import { TypeMeta } from '@kubernetes-models/base';
import { V1ConfigMap } from '@kubernetes/client-node';
import { V1CronJob } from '@kubernetes/client-node';
import { V1Deployment } from '@kubernetes/client-node';
import { V1HorizontalPodAutoscaler } from '@kubernetes/client-node';
import { V1Ingress } from '@kubernetes/client-node';
import { V1Job } from '@kubernetes/client-node';
import { V1ObjectMeta } from '@kubernetes/client-node';
import { V1Pod } from '@kubernetes/client-node';
import { V1ReplicaSet } from '@kubernetes/client-node';
import { V1Service } from '@kubernetes/client-node';
import { V1StatefulSet } from '@kubernetes/client-node';
import { WorkloadsByEntityRequest } from '@backstage/plugin-kubernetes-common';

// Warning: (ae-forgotten-export) The symbol "ClusterProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "Cluster" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const Cluster: ({
  clusterObjects,
  podsWithErrors,
}: ClusterProps) => React_2.JSX.Element;

// Warning: (ae-missing-release-tag) "ClusterContext" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const ClusterContext: React_2.Context<ClusterAttributes>;

// Warning: (ae-missing-release-tag) "ClusterLinksFormatter" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export type ClusterLinksFormatter = (
  options: ClusterLinksFormatterOptions,
) => URL;

// Warning: (ae-missing-release-tag) "ClusterLinksFormatterOptions" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface ClusterLinksFormatterOptions {
  // (undocumented)
  dashboardParameters?: JsonObject;
  // (undocumented)
  dashboardUrl?: URL;
  // (undocumented)
  kind: string;
  // (undocumented)
  object: any;
}

// Warning: (ae-missing-release-tag) "clusterLinksFormatters" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const clusterLinksFormatters: Record<string, ClusterLinksFormatter>;

// @public
export const ContainerCard: React_2.FC<ContainerCardProps>;

// @public
export interface ContainerCardProps {
  // (undocumented)
  containerMetrics?: ClientContainerStatus;
  // (undocumented)
  containerSpec?: IContainer;
  // (undocumented)
  containerStatus: IContainerStatus;
  // (undocumented)
  podScope: PodScope;
}

// @public
export interface ContainerScope extends PodScope {
  // (undocumented)
  containerName: string;
}

// Warning: (ae-forgotten-export) The symbol "CronJobsAccordionsProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "CronJobsAccordions" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const CronJobsAccordions: ({}: CronJobsAccordionsProps) => React_2.JSX.Element;

// Warning: (ae-forgotten-export) The symbol "CustomResourcesProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "CustomResources" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const CustomResources: ({}: CustomResourcesProps) => React_2.JSX.Element;

// Warning: (ae-missing-release-tag) "DeploymentResources" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface DeploymentResources {
  // (undocumented)
  deployments: V1Deployment[];
  // (undocumented)
  horizontalPodAutoscalers: V1HorizontalPodAutoscaler[];
  // (undocumented)
  pods: V1Pod[];
  // (undocumented)
  replicaSets: V1ReplicaSet[];
}

// @public
export interface DetectedError {
  // (undocumented)
  message: string;
  // (undocumented)
  occurrenceCount: number;
  // Warning: (ae-forgotten-export) The symbol "ProposedFix" needs to be exported by the entry point index.d.ts
  //
  // (undocumented)
  proposedFix?: ProposedFix;
  // (undocumented)
  severity: ErrorSeverity;
  // (undocumented)
  sourceRef: ResourceRef;
  // (undocumented)
  type: string;
}

// @public
export type DetectedErrorsByCluster = Map<string, DetectedError[]>;

// @public
export const DetectedErrorsContext: React_2.Context<DetectedError[]>;

// @public
export const detectErrors: (
  objects: ObjectsByEntityResponse,
) => DetectedErrorsByCluster;

// Warning: (ae-missing-release-tag) "EntityKubernetesContent" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const EntityKubernetesContent: (
  props: EntityKubernetesContentProps,
) => JSX.Element;

// @public
export type EntityKubernetesContentProps = {
  refreshIntervalMs?: number;
};

// @public
export const ErrorList: ({
  podAndErrors,
}: ErrorListProps) => React_2.JSX.Element;

// @public
export interface ErrorListProps {
  // (undocumented)
  podAndErrors: PodAndErrors[];
}

// @public (undocumented)
export type ErrorMatcher = {
  metadata?: IIoK8sApimachineryPkgApisMetaV1ObjectMeta;
} & TypeMeta;

// Warning: (ae-forgotten-export) The symbol "ErrorPanelProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "ErrorPanel" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const ErrorPanel: ({
  entityName,
  errorMessage,
  clustersWithErrors,
}: ErrorPanelProps) => React_2.JSX.Element;

// Warning: (ae-forgotten-export) The symbol "ErrorReportingProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "ErrorReporting" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const ErrorReporting: ({
  detectedErrors,
}: ErrorReportingProps) => React_3.JSX.Element;

// @public
export type ErrorSeverity = 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10;

// @public
export const Events: ({
  involvedObjectName,
  namespace,
  clusterName,
  warningEventsOnly,
}: EventsProps) => React_2.JSX.Element;

// @public
export const EventsContent: ({
  events,
  warningEventsOnly,
}: EventsContentProps) => React_2.JSX.Element;

// @public
export interface EventsContentProps {
  // (undocumented)
  events: Event_2[];
  // (undocumented)
  warningEventsOnly?: boolean;
}

// @public
export interface EventsOptions {
  // (undocumented)
  clusterName: string;
  // (undocumented)
  involvedObjectName: string;
  // (undocumented)
  namespace: string;
}

// @public
export interface EventsProps {
  // (undocumented)
  clusterName: string;
  // (undocumented)
  involvedObjectName: string;
  // (undocumented)
  namespace: string;
  // (undocumented)
  warningEventsOnly?: boolean;
}

// @public
export const FixDialog: React_2.FC<FixDialogProps>;

// @public
export interface FixDialogProps {
  // (undocumented)
  clusterName: string;
  // (undocumented)
  error: DetectedError;
  // (undocumented)
  open?: boolean;
  // (undocumented)
  pod: Pod;
}

// Warning: (ae-forgotten-export) The symbol "FormatClusterLinkOptions" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "formatClusterLink" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export function formatClusterLink(
  options: FormatClusterLinkOptions,
): string | undefined;

// Warning: (ae-forgotten-export) The symbol "KubernetesAuthProvider" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "GoogleKubernetesAuthProvider" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export class GoogleKubernetesAuthProvider implements KubernetesAuthProvider {
  constructor(authProvider: OAuthApi);
  // (undocumented)
  authProvider: OAuthApi;
  // (undocumented)
  decorateRequestBodyForAuth(
    requestBody: KubernetesRequestBody,
  ): Promise<KubernetesRequestBody>;
  // (undocumented)
  getCredentials(): Promise<{
    token: string;
  }>;
}

// Warning: (ae-missing-release-tag) "GroupedResponses" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface GroupedResponses extends DeploymentResources {
  // (undocumented)
  configMaps: V1ConfigMap[];
  // (undocumented)
  cronJobs: V1CronJob[];
  // (undocumented)
  customResources: any[];
  // (undocumented)
  ingresses: V1Ingress[];
  // (undocumented)
  jobs: V1Job[];
  // (undocumented)
  services: V1Service[];
  // (undocumented)
  statefulsets: V1StatefulSet[];
}

// Warning: (ae-missing-release-tag) "GroupedResponsesContext" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const GroupedResponsesContext: React_2.Context<GroupedResponses>;

// @public (undocumented)
export const HorizontalPodAutoscalerDrawer: (props: {
  hpa: V1HorizontalPodAutoscaler;
  expanded?: boolean;
  children?: React_2.ReactNode;
}) => React_2.JSX.Element;

// Warning: (ae-forgotten-export) The symbol "IngressesAccordionsProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "IngressesAccordions" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const IngressesAccordions: ({}: IngressesAccordionsProps) => React_2.JSX.Element;

// Warning: (ae-missing-release-tag) "isKubernetesAvailable" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const isKubernetesAvailable: (entity: Entity) => boolean;

// Warning: (ae-forgotten-export) The symbol "JobsAccordionsProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "JobsAccordions" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const JobsAccordions: ({
  jobs,
}: JobsAccordionsProps) => React_2.JSX.Element;

// Warning: (ae-missing-release-tag) "KubernetesApi" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface KubernetesApi {
  // (undocumented)
  getClusters(): Promise<
    {
      name: string;
      authProvider: string;
      oidcTokenProvider?: string | undefined;
    }[]
  >;
  // (undocumented)
  getCustomObjectsByEntity(
    request: CustomObjectsByEntityRequest,
  ): Promise<ObjectsByEntityResponse>;
  // (undocumented)
  getObjectsByEntity(
    requestBody: KubernetesRequestBody,
  ): Promise<ObjectsByEntityResponse>;
  // (undocumented)
  getWorkloadsByEntity(
    request: WorkloadsByEntityRequest,
  ): Promise<ObjectsByEntityResponse>;
  // (undocumented)
  proxy(options: {
    clusterName: string;
    path: string;
    init?: RequestInit;
  }): Promise<Response>;
}

// Warning: (ae-missing-release-tag) "kubernetesApiRef" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const kubernetesApiRef: ApiRef<KubernetesApi>;

// Warning: (ae-missing-release-tag) "KubernetesAuthProviders" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export class KubernetesAuthProviders implements KubernetesAuthProvidersApi {
  constructor(options: {
    microsoftAuthApi: OAuthApi;
    googleAuthApi: OAuthApi;
    oidcProviders?: {
      [key: string]: OpenIdConnectApi;
    };
  });
  // (undocumented)
  decorateRequestBodyForAuth(
    authProvider: string,
    requestBody: KubernetesRequestBody,
  ): Promise<KubernetesRequestBody>;
  // (undocumented)
  getCredentials(authProvider: string): Promise<{
    token?: string;
  }>;
}

// Warning: (ae-missing-release-tag) "KubernetesAuthProvidersApi" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface KubernetesAuthProvidersApi {
  // (undocumented)
  decorateRequestBodyForAuth(
    authProvider: string,
    requestBody: KubernetesRequestBody,
  ): Promise<KubernetesRequestBody>;
  // (undocumented)
  getCredentials(authProvider: string): Promise<{
    token?: string;
  }>;
}

// Warning: (ae-missing-release-tag) "kubernetesAuthProvidersApiRef" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const kubernetesAuthProvidersApiRef: ApiRef<KubernetesAuthProvidersApi>;

// Warning: (ae-missing-release-tag) "KubernetesBackendClient" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export class KubernetesBackendClient implements KubernetesApi {
  constructor(options: {
    discoveryApi: DiscoveryApi;
    identityApi: IdentityApi;
    kubernetesAuthProvidersApi: KubernetesAuthProvidersApi;
  });
  // (undocumented)
  getClusters(): Promise<
    {
      name: string;
      authProvider: string;
    }[]
  >;
  // (undocumented)
  getCustomObjectsByEntity(
    request: CustomObjectsByEntityRequest,
  ): Promise<ObjectsByEntityResponse>;
  // (undocumented)
  getObjectsByEntity(
    requestBody: KubernetesRequestBody,
  ): Promise<ObjectsByEntityResponse>;
  // (undocumented)
  getWorkloadsByEntity(
    request: WorkloadsByEntityRequest,
  ): Promise<ObjectsByEntityResponse>;
  // (undocumented)
  proxy(options: {
    clusterName: string;
    path: string;
    init?: RequestInit;
  }): Promise<Response>;
}

// Warning: (ae-forgotten-export) The symbol "KubernetesContentProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "KubernetesContent" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const KubernetesContent: ({
  entity,
  refreshIntervalMs,
}: KubernetesContentProps) => React_2.JSX.Element;

// Warning: (ae-forgotten-export) The symbol "KubernetesDrawerProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "KubernetesDrawer" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const KubernetesDrawer: ({
  open,
  label,
  drawerContentsHeader,
  kubernetesObject,
  children,
}: KubernetesDrawerProps) => React_2.JSX.Element;

// Warning: (ae-forgotten-export) The symbol "KubernetesDrawerContentProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "KubernetesDrawerContent" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const KubernetesDrawerContent: ({
  children,
  header,
  kubernetesObject,
  close,
}: KubernetesDrawerContentProps) => React_2.JSX.Element;

// Warning: (ae-missing-release-tag) "KubernetesObjects" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface KubernetesObjects {
  // (undocumented)
  error?: string;
  // (undocumented)
  kubernetesObjects?: ObjectsByEntityResponse;
  // (undocumented)
  loading: boolean;
}

// Warning: (ae-missing-release-tag) "kubernetesPlugin" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
const kubernetesPlugin: BackstagePlugin<
  {
    entityContent: RouteRef<undefined>;
  },
  {},
  {}
>;
export { kubernetesPlugin };
export { kubernetesPlugin as plugin };

// Warning: (ae-missing-release-tag) "KubernetesProxyApi" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface KubernetesProxyApi {
  // (undocumented)
  getEventsByInvolvedObjectName(request: {
    clusterName: string;
    involvedObjectName: string;
    namespace: string;
  }): Promise<Event_2[]>;
  // (undocumented)
  getPodLogs(request: {
    podName: string;
    namespace: string;
    clusterName: string;
    containerName: string;
    previous?: boolean;
  }): Promise<{
    text: string;
  }>;
}

// Warning: (ae-missing-release-tag) "kubernetesProxyApiRef" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const kubernetesProxyApiRef: ApiRef<KubernetesProxyApi>;

// @public
export class KubernetesProxyClient {
  constructor(options: { kubernetesApi: KubernetesApi });
  // (undocumented)
  getEventsByInvolvedObjectName({
    clusterName,
    involvedObjectName,
    namespace,
  }: {
    clusterName: string;
    involvedObjectName: string;
    namespace: string;
  }): Promise<Event_2[]>;
  // (undocumented)
  getPodLogs({
    podName,
    namespace,
    clusterName,
    containerName,
    previous,
  }: {
    podName: string;
    namespace: string;
    clusterName: string;
    containerName: string;
    previous?: boolean;
  }): Promise<{
    text: string;
  }>;
}

// Warning: (ae-forgotten-export) The symbol "KubernetesDrawerable" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "KubernetesStructuredMetadataTableDrawerProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "KubernetesStructuredMetadataTableDrawer" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const KubernetesStructuredMetadataTableDrawer: <
  T extends KubernetesDrawerable,
>({
  object,
  renderObject,
  kind,
  buttonVariant,
  expanded,
  children,
}: KubernetesStructuredMetadataTableDrawerProps<T>) => React_2.JSX.Element;

// Warning: (ae-forgotten-export) The symbol "ErrorPanelProps_2" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "LinkErrorPanel" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const LinkErrorPanel: ({
  cluster,
  errorMessage,
}: ErrorPanelProps_2) => React_2.JSX.Element;

// @public
export const PendingPodContent: ({
  pod,
}: PendingPodContentProps) => React_2.JSX.Element;

// @public
export interface PendingPodContentProps {
  // (undocumented)
  pod: Pod_2;
}

// @public
export interface PodAndErrors {
  // (undocumented)
  clusterName: string;
  // (undocumented)
  errors: DetectedError[];
  // (undocumented)
  pod: Pod_2;
}

// Warning: (ae-forgotten-export) The symbol "PodDrawerProps" needs to be exported by the entry point index.d.ts
//
// @public
export const PodDrawer: ({
  podAndErrors,
  open,
}: PodDrawerProps) => React_2.JSX.Element;

// @public
export const PodExecTerminal: (
  props: PodExecTerminalProps,
) => React_2.JSX.Element;

// @public
export const PodExecTerminalDialog: (
  props: PodExecTerminalProps,
) => React_2.JSX.Element;

// @public
export interface PodExecTerminalProps {
  // (undocumented)
  clusterName: string;
  // (undocumented)
  containerName: string;
  // (undocumented)
  podName: string;
  // (undocumented)
  podNamespace: string;
}

// @public
export const PodLogs: React_2.FC<PodLogsProps>;

// @public
export const PodLogsDialog: ({
  containerScope,
}: PodLogsDialogProps) => React_2.JSX.Element;

// @public
export interface PodLogsDialogProps {
  // (undocumented)
  containerScope: ContainerScope;
}

// @public
export interface PodLogsOptions {
  // (undocumented)
  containerScope: ContainerScope;
  // (undocumented)
  previous?: boolean;
}

// @public
export interface PodLogsProps {
  // (undocumented)
  containerScope: ContainerScope;
  // (undocumented)
  previous?: boolean;
}

// @public
export const PodMetricsContext: React_2.Context<Map<string, ClientPodStatus[]>>;

// Warning: (ae-missing-release-tag) "PodMetricsMatcher" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export type PodMetricsMatcher = {
  metadata?: IObjectMeta;
};

// Warning: (ae-missing-release-tag) "PodNamesWithErrorsContext" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const PodNamesWithErrorsContext: React_2.Context<Set<string>>;

// Warning: (ae-missing-release-tag) "PodNamesWithMetricsContext" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const PodNamesWithMetricsContext: React_2.Context<
  Map<string, ClientPodStatus>
>;

// @public
export interface PodScope {
  // (undocumented)
  clusterName: string;
  // (undocumented)
  podName: string;
  // (undocumented)
  podNamespace: string;
}

// Warning: (ae-forgotten-export) The symbol "PodsTablesProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "PodsTable" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const PodsTable: ({
  pods,
  extraColumns,
}: PodsTablesProps) => React_2.JSX.Element;

// @public
export interface ResourceRef {
  // (undocumented)
  apiGroup: string;
  // (undocumented)
  kind: string;
  // (undocumented)
  name: string;
  // (undocumented)
  namespace: string;
}

// Warning: (ae-forgotten-export) The symbol "ResourceUtilizationProps" needs to be exported by the entry point index.d.ts
//
// @public
export const ResourceUtilization: ({
  compressed,
  title,
  usage,
  total,
  totalFormatted,
}: ResourceUtilizationProps) => React_2.JSX.Element;

// Warning: (ae-missing-release-tag) "Router" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const Router: (props: {
  refreshIntervalMs?: number;
}) => React_2.JSX.Element;

// @public
export class ServerSideKubernetesAuthProvider
  implements KubernetesAuthProvider
{
  // (undocumented)
  decorateRequestBodyForAuth(
    requestBody: KubernetesRequestBody,
  ): Promise<KubernetesRequestBody>;
  // (undocumented)
  getCredentials(): Promise<{}>;
}

// Warning: (ae-forgotten-export) The symbol "ServicesAccordionsProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "ServicesAccordions" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const ServicesAccordions: ({}: ServicesAccordionsProps) => React_2.JSX.Element;

// @public
export const useCustomResources: (
  entity: Entity,
  customResourceMatchers: CustomResourceMatcher[],
  intervalMs?: number,
) => KubernetesObjects;

// @public
export const useEvents: ({
  involvedObjectName,
  namespace,
  clusterName,
}: EventsOptions) => AsyncState<Event_2[]>;

// Warning: (ae-missing-release-tag) "useKubernetesObjects" is part of the package's API, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const useKubernetesObjects: (
  entity: Entity,
  intervalMs?: number,
) => KubernetesObjects;

// @public
export const useMatchingErrors: (matcher: ErrorMatcher) => DetectedError[];

// @public
export const usePodLogs: ({
  containerScope,
  previous,
}: PodLogsOptions) => AsyncState<{
  text: string;
}>;

// @public
export const usePodMetrics: (
  clusterName: string,
  matcher: PodMetricsMatcher,
) => ClientPodStatus | undefined;
```
